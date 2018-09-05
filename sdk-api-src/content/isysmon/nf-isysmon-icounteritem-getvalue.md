---
UID: NF:isysmon.ICounterItem.GetValue
title: GetValue function
author: windows-sdk-content
description: Retrieves the last value of the counter.
old-location: sysmon\counteritem_getvalue.htm
old-project: SysMon
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CounterItem object [SysMon],GetValue method, CounterItem,GetValue, CounterItem.GetValue, GetValue, GetValue method [SysMon], GetValue method [SysMon],CounterItem object, GetValue,CounterItem, _win32_counteritem.getvalue, base.counteritem_getvalue, sysmon.counteritem_getvalue
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
 - CounterItem.GetValue
product: Windows
targetos: Windows
req.lib: 
req.dll: Sysmon.ocx
req.irql: 
req.product: GDI+ 1.1
---

# GetValue function


## -description


Retrieves the last value of the counter.
		


## -parameters




### -param Value

TBD


### -param Status

TBD




#### - status [out]

Indicates if the value is valid.
					

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
The value is valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0xC0000BBA (3221228474)</dt>
</dl>
</td>
<td width="60%">
The value is not valid.

</td>
</tr>
</table>
 


#### - value [out]

Last sampled value of the counter.


## -returns



This method does not return a value.




## -remarks



If the source of the counter data is from a log file, the value is the last counter value in the log file.




## -see-also




<a href="https://msdn.microsoft.com/76b69395-efd8-4321-b7ed-63daa46e2636">CounterItem</a>



<a href="https://msdn.microsoft.com/fb55d68b-1dbe-48b1-88c8-51f33048ec24">CounterItem.GetStatistics</a>



<a href="https://msdn.microsoft.com/c5aeaa00-e185-484d-8a7a-d45a21690e20">CounterItem.Value</a>
 

 

