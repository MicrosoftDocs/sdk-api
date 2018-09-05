---
UID: NF:isysmon.ICounterItem.GetStatistics
title: GetStatistics function
author: windows-sdk-content
description: Retrieves the average, maximum, and minimum values for the counter.
old-location: sysmon\counteritem_getstatistics.htm
old-project: SysMon
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CounterItem object [SysMon],GetStatistics method, CounterItem,GetStatistics, CounterItem.GetStatistics, GetStatistics, GetStatistics method [SysMon], GetStatistics method [SysMon],CounterItem object, GetStatistics,CounterItem, _win32_counteritem.getstatistics, base.counteritem_getstatistics, sysmon.counteritem_getstatistics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: isysmon.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SysmonBatchReason
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sysmon.ocx
api_name:
 - CounterItem.GetStatistics
product: Windows
targetos: Windows
req.lib: 
req.dll: Sysmon.ocx
req.irql: 
req.product: GDI+ 1.1
---

# GetStatistics function


## -description


Retrieves the average, maximum, and minimum values for the counter.
		


## -parameters




### -param Max

TBD


### -param Min

TBD


### -param Avg

TBD


### -param Status

TBD




#### - average [out]

Average value of the counter.


#### - max [out]

Maximum value of the counter.


#### - min [out]

Minimum value of the counter.


#### - status [out]

Indicates if the values are valid.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The values are valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0xC0000BBA (3221228474)</dt>
</dl>
</td>
<td width="60%">
The values are not valid.

</td>
</tr>
</table>
 


## -returns



This method does not return a value.




## -remarks



Only those counter values that are visible in the graph window are used to calculate the statistical values.




## -see-also




<a href="https://msdn.microsoft.com/76b69395-efd8-4321-b7ed-63daa46e2636">CounterItem</a>



<a href="https://msdn.microsoft.com/e8484301-4575-41ee-9c6d-a454eca0e82d">CounterItem.GetDataAt</a>



<a href="https://msdn.microsoft.com/cf50d878-a119-42b0-bc59-b0e37ed15321">CounterItem.GetValue</a>
 

 

