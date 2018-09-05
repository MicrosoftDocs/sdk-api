---
UID: NF:isysmon.ICounterItem2.GetDataAt
title: GetDataAt function
author: windows-sdk-content
description: Retrieves the specified counter value from a specific point in the graph.
old-location: sysmon\counteritem_getdataat.htm
old-project: SysMon
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CounterItem object [Performance Monitoring],GetDataAt method, CounterItem object [SysMon],GetDataAt method, CounterItem.GetDataAt, GetDataAt, GetDataAt method [Performance Monitoring], GetDataAt method [Performance Monitoring],CounterItem object, GetDataAt method [SysMon], GetDataAt method [SysMon],CounterItem object, base.counteritem_getdataat, sysmon.counteritem_getdataat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: isysmon.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - CounterItem.GetDataAt
product: Windows
targetos: Windows
req.lib: 
req.dll: Sysmon.ocx
req.irql: 
req.product: GDI+ 1.1
---

# GetDataAt function


## -description


Retrieves the specified counter value from a specific point in the graph.


## -parameters




### -param iIndex

TBD


### -param iWhich

TBD


### -param pVariant

TBD




#### - index [in]

Zero-based index of the graph point whose value you want to retrieve. Valid values range from 0 to (<a href="https://msdn.microsoft.com/bc1a86c2-635b-4e93-ac96-e7be4b1d375a">SystemMonitor.DataPointCount</a> - 1).


#### - variant [out]

Counter value that was retrieved.


#### - which [in]

Type of counter value to retrieve, for example, the average value of the counter as displayed in the graph window. For possible values, see <a href="https://msdn.microsoft.com/5855fffc-1113-4047-b55a-601e45a08a5e">SysmonDataType</a>. 


## -returns



This method does not return a value.




## -remarks



Use this method only if

<ul>
<li>
<a href="https://msdn.microsoft.com/a04545b1-920e-4fb3-909b-dc47e1374629">SystemMonitor.DisplayType</a> is set to sysmonLineGraph</li>
<li>
<a href="https://msdn.microsoft.com/53c1e9bc-dafd-445c-8d82-13a74f6c488a">SystemMonitor.DataSourceType</a> is set to sysmonLogFiles or sysmonSqlLog</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/76b69395-efd8-4321-b7ed-63daa46e2636">CounterItem</a>



<a href="https://msdn.microsoft.com/fb55d68b-1dbe-48b1-88c8-51f33048ec24">CounterItem.GetStatistics</a>



<a href="https://msdn.microsoft.com/cf50d878-a119-42b0-bc59-b0e37ed15321">CounterItem.GetValue</a>
 

 

