---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMonthlyTrigger::get_DaysOfMonth


## -description


Gets or sets the days of the month during which the task runs.

This property is read/write.


## -parameters


## -remarks




<table>
<tr>
<th>Day of month</th>
<th>Hex value</th>
<th>Decimal value</th>
</tr>
<tr>
<td>1</td>
<td>0x01</td>
<td>1</td>
</tr>
<tr>
<td>2</td>
<td>0x02</td>
<td>2</td>
</tr>
<tr>
<td>3</td>
<td>0x04</td>
<td>4</td>
</tr>
<tr>
<td>4</td>
<td>0x08</td>
<td>8</td>
</tr>
<tr>
<td>5</td>
<td>0x10</td>
<td>16</td>
</tr>
<tr>
<td>6</td>
<td>0x20</td>
<td>32</td>
</tr>
<tr>
<td>7</td>
<td>0x40</td>
<td>64</td>
</tr>
<tr>
<td>8</td>
<td>0x80</td>
<td>128</td>
</tr>
<tr>
<td>9</td>
<td>0x100</td>
<td>256</td>
</tr>
<tr>
<td>10</td>
<td>0x200</td>
<td>512</td>
</tr>
<tr>
<td>11</td>
<td>0x400</td>
<td>1024</td>
</tr>
<tr>
<td>12</td>
<td>0x800</td>
<td>2048</td>
</tr>
<tr>
<td>13</td>
<td>0x1000</td>
<td>4096</td>
</tr>
<tr>
<td>14</td>
<td>0x2000</td>
<td>8192</td>
</tr>
<tr>
<td>15</td>
<td>0x4000</td>
<td>16384</td>
</tr>
<tr>
<td>16</td>
<td>0x8000</td>
<td>32768</td>
</tr>
<tr>
<td>17</td>
<td>0x10000</td>
<td>65536</td>
</tr>
<tr>
<td>18</td>
<td>0x20000</td>
<td>131072</td>
</tr>
<tr>
<td>19</td>
<td>0x40000</td>
<td>262144</td>
</tr>
<tr>
<td>20</td>
<td>0x80000</td>
<td>524288</td>
</tr>
<tr>
<td>21</td>
<td>0x100000</td>
<td>1048576</td>
</tr>
<tr>
<td>22</td>
<td>0x200000</td>
<td>2097152</td>
</tr>
<tr>
<td>23</td>
<td>0x400000</td>
<td>4194304</td>
</tr>
<tr>
<td>24</td>
<td>0x800000</td>
<td>8388608</td>
</tr>
<tr>
<td>25</td>
<td>0x1000000</td>
<td>16777216</td>
</tr>
<tr>
<td>26</td>
<td>0x2000000</td>
<td>33554432</td>
</tr>
<tr>
<td>27</td>
<td>0x4000000</td>
<td>67108864</td>
</tr>
<tr>
<td>28</td>
<td>0x8000000</td>
<td>134217728</td>
</tr>
<tr>
<td>29</td>
<td>0x10000000</td>
<td>268435456</td>
</tr>
<tr>
<td>30</td>
<td>0x20000000</td>
<td>536870912</td>
</tr>
<tr>
<td>31</td>
<td>0x40000000</td>
<td>1073741824</td>
</tr>
<tr>
<td>Last</td>
<td>0x80000000</td>
<td>2147483648</td>
</tr>
</table>
 



When reading or writing your own XML for a task, the days of the month are specified using the <a href="https://msdn.microsoft.com/62f28f44-b3d8-414e-80d4-f4d8bd3c4527">DaysOfMonth</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/2ed206a6-22e0-4131-92ce-29536ad65c6c">IMonthlyTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

