---
UID: NE:isysmon.__MIDL___MIDL_itf_sysmon_0000_0000_0002
title: SysmonDataType (isysmon.h)
author: windows-sdk-content
description: Determines the type of data to return from a given data point on the graph.
old-location: sysmon\sysmondatatype.htm
tech.root: SysMon
ms.assetid: 5855fffc-1113-4047-b55a-601e45a08a5e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SysmonDataType, SysmonDataType enumeration [SysMon], base.sysmondatatype, isysmon/SysmonDataType, isysmon/sysmonDataAvg, isysmon/sysmonDataCount, isysmon/sysmonDataMax, isysmon/sysmonDataMin, isysmon/sysmonDataTime, sysmon.sysmondatatype, sysmonDataAvg, sysmonDataCount, sysmonDataMax, sysmonDataMin, sysmonDataTime
ms.topic: enum
f1_keywords: 
 - "isysmon/SysmonDataType"
req.header: isysmon.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ISysmon.h
api_name:
 - SysmonDataType
targetos: Windows
req.typenames: SysmonDataType
req.redist: 
ms.custom: 19H1
---

# SysmonDataType enumeration


## -description


Determines the type of data to return from a given data point on the graph.


## -enum-fields




### -field sysmonDataAvg

Average value of the counter.


### -field sysmonDataMin

Minimum value of the counter.


### -field sysmonDataMax

Maximum value of the counter.


### -field sysmonDataTime

Date and time that the counter value was collected. If SYSMON compresses more than one sample into the counter value, the date and time are from the last sample.


### -field sysmonDataCount

Number of samples that were compressed into the data point.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SysMon/counteritem-getdataat">CounterItem.GetDataAt</a>
 

 

