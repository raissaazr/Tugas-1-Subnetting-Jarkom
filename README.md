# Tugas-1-Subnetting-Jarkom
| Nama                         | NRP        |
| ---------------------------- | ---------- |
| Azaria Raissa Maulidinnisa   | 5027241043 |

# Topologi

<img width="893" height="397" alt="Screenshot 2025-11-11 142946" src="https://github.com/user-attachments/assets/27b6ce5f-ae69-49fa-8027-73ba18c4fc06" />

# Subnet
| Subnet                          | Kebutuhan  | Prefix  |
| ------------------------------- | -----------| ------- |
| Bidang Guru & Tendik            | 96 host    | /25     |
| Bidang Kurikulum                | 221 host   | /24     |
| Bidang Sarana Prasarana         | 46 host    | /26     |
| Server & Admin                  | 7 host     | /28     |
| Sekretariat                     | 381 host   | /23     |
| Bidang Pengawas Sekolah (Branch)| 19 host    | /27     |
| Router                          | 2 host     | /30     |
| Total                           | 772 host   | /22     |

IP Prefix : ``10.83.0.0/22`` </br>
Total host : 772 host

# Tabel VLSM 
| Subnet                          |Total IP	| Available Host |Prefix | Netmask         |	NID        | Broadcast    |	Range IP Available	      |Gateway    |
|---------------------------------|---------|----------------|-------|-----------------|-------------|--------------|---------------------------|-----------|
| Sekretariat                     |512	    | 510	           | /23	 | 255.255.254.0   | 10.83.0.0	 | 10.83.1.255  | 10.83.0.1 - 10.83.1.254   |10.83.0.1  |
| Bidang Kurikulum                |256	    | 254            | /24   | 255.255.255.0   | 10.83.2.0	 | 10.83.2.255  | 10.83.2.1 - 10.83.2.254	  |10.83.2.1  |
| Bidang Guru & Tendik            |128	    | 126            | /25	 | 255.255.255.128 | 10.83.3.0	 | 10.83.3.127  | 10.83.3.1 - 10.83.3.126	  |10.83.3.1  |
| Bidang Sarana Prasarana         |64	      | 62	           | /26	 | 255.255.255.192 | 10.83.3.128 | 10.83.3.191  | 10.83.3.129 - 10.83.3.190 |10.83.3.129|
| Bidang Pengawas Sekolah (Branch)|32	      | 30	           | /27	 | 255.255.255.224 | 10.83.3.192 | 10.83.3.223  | 10.83.3.193 - 10.83.3.222 |10.83.3.193|
| Server & Admin                  |16       |	14	           | /28	 | 255.255.255.240 | 10.83.3.224 | 10.83.3. 239 |	10.83.3.225 - 10.83.3.238	|10.83.3.225|
| Router                          |4	      | 2              | /30	 | 255.255.255.252 | 10.83.3.240 |10.83.3.243   | 10.83.3.241 - 10.83.3.242	|10.83.3.241|

# Tabel CIDR
| Subnet                                         |Total IP	| Available Host |Prefix | Netmask         |	NID        | Broadcast    |	Range IP Available	      |Gateway      |
|------------------------------------------------|----------|----------------|-------|-----------------|-------------|--------------|---------------------------|-------------|
| Sekretariat, Kurikulum, Guru & Tendik, Sarpras |1024	    | 1022	         | /22	 | 255.255.252.0   | 10.83.0.0	 | 10.83.3.191  | 10.83.0.1 - 10.83.3.190   |10.83.0.1    |
| Kantor cabang, Router                          |64	      | 62             | /26   | 255.255.255.192 | 10.83.3.192 | 10.83.3.255  | 10.83.3.193 - 10.83.3.254 |10.83.3.193  |
| Server & Admin                                 |16        |	14	           | /28	 | 255.255.255.240 | 10.83.3.224 | 10.83.3. 239 |	10.83.3.225 - 10.83.3.238	|10.83.3.225  |
