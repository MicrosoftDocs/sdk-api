---
UID: NC:routprot.PMIB_GET_TRAP_INFO
title: PMIB_GET_TRAP_INFO
author: windows-driver-content
description: The MibGetTrapInfo function queries the module that set a trap event for more information about the trap.
old-location: rras\mibgettrapinfo.htm
old-project: RRAS
ms.assetid: 2eb77b83-27bb-414b-8fbf-519d5e0cb08a
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: MibGetTrapInfo, MibGetTrapInfo callback function [RAS], PMIB_GET_TRAP_INFO, PMIB_GET_TRAP_INFO callback, _mpr_mibgettrapinfo, routprot/MibGetTrapInfo, rras.mibgettrapinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: routprot.h
req.include-header: 
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Routprot.h
api_name:
-	MibGetTrapInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PMIB_GET_TRAP_INFO callback function


## -description


The <b>MibGetTrapInfo</b> function queries the module that set a trap event for more information about the trap.

The <a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">PMIB_GET_TRAP_INFO</a> type defines a pointer to this callback function. <i>MibGetTrapInfo</i> is a placeholder for the application-defined function name.


## -parameters




### -param InputDataSize [in]

Specifies a <b>ULONG</b> variable that specifies the size in bytes of the data pointed to by <i>InputData</i>.


### -param InputData [in]

Pointer to the input data.


### -param OutputDataSize [out]

Pointer to a <b>ULONG</b> variable that receives the size in bytes of the data pointed to by * <i>OutputData</i>.


### -param OutputData [out]

Receives the address of a pointer to the output data.


## -returns



If the functions succeeds, the return value is NO_ERROR

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient resources to complete the operation.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/28056113-82a5-4493-ba49-509db3606fa0">MibSetTrapInfo</a>
 

 

