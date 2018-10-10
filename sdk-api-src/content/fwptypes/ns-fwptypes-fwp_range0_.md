---
UID: NS:fwptypes.FWP_RANGE0_
title: FWP_RANGE0_
author: windows-sdk-content
description: Specifies a range of values.
old-location: fwp\fwp_range0.htm
tech.root: FWP
ms.assetid: 191ec0e4-2489-4f6f-80c5-8feec83d69c2
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: FWP_RANGE0, FWP_RANGE0 structure [Filtering], FWP_RANGE0_, fwp.fwp_range0, fwptypes/FWP_RANGE0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwptypes.idl
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
 - Fwptypes.h
api_name:
 - FWP_RANGE0
product: Windows
targetos: Windows
req.typenames: FWP_RANGE0
req.redist: 
---

# FWP_RANGE0_ structure


## -description


The <b>FWP_RANGE0</b> structure specifies a range of values.


## -struct-fields




### -field valueLow

Low value of the range.

See <a href="https://msdn.microsoft.com/d3ffe19b-2c9b-4c7b-82c1-f9b846546212">FWP_VALUE0</a> for more information.


### -field valueHigh

High value of the range.

See <a href="https://msdn.microsoft.com/d3ffe19b-2c9b-4c7b-82c1-f9b846546212">FWP_VALUE0</a> for more information.


## -remarks



The elements <b>valueLow</b> and <b>valueHigh</b> must be the same data type and 
<b>valueHigh</b> must be greater than or equal to <b>valueLow</b>. 

Ranges are always inclusive. Thus, if a value equals
<b>valueLow</b> or <b>valueHigh</b>, it is contained in the range.

<b>FWP_RANGE0</b> is a specific implementation of FWP_RANGE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/d3ffe19b-2c9b-4c7b-82c1-f9b846546212">FWP_VALUE0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

