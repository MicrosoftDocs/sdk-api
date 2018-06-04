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

# _MIB_IF_TABLE_LEVEL enumeration


## -description


The MIB_IF_TABLE_LEVEL enumeration type defines the level of interface information to
  retrieve.


## -enum-fields




### -field MibIfTableNormal

The values of statistics and state that are returned in members of the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure in the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a> structure that the 
     <i>Table</i> parameter points to in the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552528">GetIfTable2Ex</a> function are returned from
     the top of the filter stack.


### -field MibIfTableRaw

The values of statistics and state that are returned in members of the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a> structure in the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a> structure that the 
     <i>Table</i> parameter points to in the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552528">GetIfTable2Ex</a> function are returned
     directly for the interface that is being queried.


### -field MibIfTableNormalWithoutStatistics

<div class="alert"><b>Note</b>  This value is available starting with Windows 10, version 1703.</div>
<div> </div>
The values returned are the same as for the <b>MibIfTableNormal </b> value, but without the statistics.


## -remarks



The MIB_IF_TABLE_LEVEL enumeration type is used with the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff552528">GetIfTable2Ex</a> function to specify the level
    of interface information to retrieve.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552528">GetIfTable2Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559214">MIB_IF_ROW2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559224">MIB_IF_TABLE2</a>
 

 

