<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sports Events</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        th, td {
            padding: 10px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }

        th {
            background-color: #f2f2f2;
        }

        a {
            text-decoration: none;
            color: #007bff;
        }

        a:hover {
            text-decoration: underline;
        }

        #search {
            margin-bottom: 20px;
        }

        .content {
            display: none;
        }

        .active {
            display: table-row;
        }

        .bilingual {
            font-size: 80%;
            color: #555;
        }
    </style>
    <script>
        function showContent(id) {
            var content = document.getElementsByClassName("content");
            for (var i = 0; i < content.length; i++) {
                content[i].classList.remove("active");
            }

            document.getElementById(id).classList.add("active");
        }

        function search() {
            var input, filter, table, tr, td, i, txtValue;
            input = document.getElementById("searchInput");
            filter = input.value.toUpperCase();
            table = document.getElementById("eventTable");
            tr = table.getElementsByTagName("tr");
            for (i = 0; i < tr.length; i++) {
                td = tr[i].getElementsByTagName("td")[0];
                if (td) {
                    txtValue = td.textContent || td.innerText;
                    if (txtValue.toUpperCase().indexOf(filter) > -1) {
                        tr[i].style.display = "";
                    } else {
                        tr[i].style.display = "none";
                    }
                }
            }
        }

        function openEvent(eventId) {
            showContent(eventId);
        }
    </script>
</head>
<body>
    <h1>Sports Events</h1>
    <div id="search">
        <input type="text" id="searchInput" placeholder="Search for an event..." onkeyup="search()">
    </div>
    <table id="eventTable">
        <tr>
            <th>Event</th>
            <th>Date</th>
            <th>Time</th>
        </tr>
        <tr onclick="showContent('fencing')">
            <td>
                <a href="javascript:void(0);">Fencing</a>
                <span class="bilingual">المبارزة</span>
            </td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr class="content" id="fencing">
            <td colspan="3">
                <table>
                    <tr>
                        <th>Event</th>
                        <th>Date</th>
                        <th>Time</th>
                    </tr>
                    <tr>
                        <td>Women Foil Individual</td>
                        <td>2023.9.25</td>
                        <td>12:30 (Knockout), 18:45 (Semifinal), 12:30 (Finals)</td>
                    </tr>
                    <tr>
                        <td>Women Epee Individual</td>
                        <td>2023.9.24</td>
                        <td>12:30 (Knockout), 19:05 (Semifinal), 20:45 (Finals)</td>
                    </tr>
                    <tr>
                        <td>Man Epee Individual</td>
                        <td>2023.9.26</td>
                        <td>12:30 (Knockout), 19:15 (Semifinals), 20:45 (Finals)</td>
                    </tr>
                    <tr>
                        <td>Man Epee Team</td>
                        <td>2023.9.29</td>
                        <td>12:00 (Knockout), 16:00 (Semifinals), 18:35 (Finals)</td>
                    </tr>
                </table>
            </td>
        </tr>
        <!-- Cycling Track -->
        <tr onclick="showContent('cycling-track')">
            <td>
                <a href="javascript:void(0);">Cycling Track</a>
                <span class="bilingual">دراجات السباق</span>
            </td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr class="content" id="cycling-track">
            <td colspan="3">
                <table>
                    <tr>
                        <th>Event</th>
                        <th>Date</th>
                        <th>Time</th>
                    </tr>
                    <tr>
                        <td>Man Team Pursuit</td>
                        <td>2023.9.26</td>
                        <td>10:00-12:46 (Qualification Tournament), 15:00-17:22 (The First Round), 15:00-17:22 (Finals)</td>
                    </tr>
                    <tr>
                        <td>Man Keirin</td>
                        <td>2023.9.29</td>
                        <td>14:00-15:36 (The First Round), 14:00-15:36 (Repechange), 18:00-21:37 (1/2 Finals), 18:00-21:37 (Finals)</td>
                    </tr>
                    <tr>
                        <td>Man Madison</td>
                        <td>2023.9.29</td>
                        <td>18:00-21:37 (Finals)</td>
                    </tr>
                    <tr>
                        <td>Man Omnium</td>
                        <td>2023.9.28</td>
                        <td>10:00-12:01 (1/4, 2/4 Tournament), 15:00-19:22 (3/4, 4/4 Tournament)</td>
                    </tr>
                </table>
            </td>
        </tr>
        <!-- Cycling Mountain Bike -->
        <tr onclick="showContent('cycling-mountain-bike')">
            <td>
                <a href="javascript:void(0);">Cycling Mountain Bike</a>
                <span class="bilingual">دراجات جبال السباق</span>
            </td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr class="content" id="cycling-mountain-bike">
            <td colspan="3">
                <table>
                    <tr>
                        <th>Event</th>
                        <th>Date</th>
                        <th>Time</th>
                    </tr>
                    <tr>
                        <td>Cycling Mountain Bike</td>
                        <td>2023.9.25</td>
                        <td>13:30-15:30 (Finals)</td>
                    </tr>
                </table>
            </td>
        </tr>
        <!-- Equestrian -->
        <tr onclick="showContent('equestrian')">
            <td>
                <a href="javascript:void(0);">Equestrian</a>
                <span class="bilingual">الفروسية</span>
            </td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr class="content" id="equestrian">
            <td colspan="3">
                <table>
                    <tr>
                        <th>Event</th>
                        <th>Date</th>
                        <th>Time</th>
                    </tr>
                    <tr>
                        <td>Dressage Individual - Qualification Tournament</td>
                        <td>2023.9.27</td>
                        <td>8:00-12:00, 14:00-17:00</td>
                    </tr>
                    <tr>
                        <td>Dressage Team - Qualification Tournament</td>
                        <td>2023.9.26</td>
                        <td>8:00-12:00, 14:00-17:00</td>
                    </tr>
                    <tr>
                        <td>Jumping Team - Qualification Tournament</td>
                        <td>2023.10.4</td>
                        <td>9:00-12:00, 14:00-17:00</td>
                    </tr>
                    <tr>
                        <td>Jumping Individual</td>
                        <td>&nbsp;</td>
                        <td>&nbsp;</td>
                    </tr>
                    <tr>
                        <td>Jumping Individual - Finals</td>
                        <td>2023.10.6</td>
                        <td>9:00-11:00, 15:00-17:00</td>
                    </tr>
                </table>
            </td>
        </tr>
    </table>
</body>
</html>
