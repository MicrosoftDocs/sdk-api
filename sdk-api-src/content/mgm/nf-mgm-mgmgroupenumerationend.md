---
UID: NF:mgm.MgmGroupEnumerationEnd
title: MgmGroupEnumerationEnd function
author: windows-sdk-content
description: The MgmGroupEnumerationEnd function releases the specified enumeration handle that was obtained from a previous call to MgmGroupEnumerationStart.
old-location: rras\mgmgroupenumerationend.htm
old-project: rras
ms.assetid: 87a0bd96-c877-443e-a539-a31ab0971869
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MgmGroupEnumerationEnd, MgmGroupEnumerationEnd function [RAS], _mpr_mgmgroupenumerationend, mgm/MgmGroupEnumerationEnd, rras.mgmgroupenumerationend
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mgm.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: MGM_ENUM_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - MgmGroupEnumerationEnd
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: GDI+ 1.1
---

# MgmGroupEnumerationEnd function


## -description


The 
<b>MgmGroupEnumerationEnd</b> function releases the specified enumeration handle that was obtained from a previous call to 
<a href="https://msdn.microsoft.com/926f4055-becb-4c99-afd2-2d2822626f24">MgmGroupEnumerationStart</a>.


## -parameters




### -param hEnum [in]

Specifies the enumeration handle to release.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the call to this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid enumeration handle.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/a5e659e9-b566-490b-831b-96f9de822ebf">MgmGroupEnumerationGetNext</a>



<a href="https://msdn.microsoft.com/926f4055-becb-4c99-afd2-2d2822626f24">MgmGroupEnumerationStart</a>
 

 

