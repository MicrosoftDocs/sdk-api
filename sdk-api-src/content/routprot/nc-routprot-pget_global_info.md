---
UID: NC:routprot.PGET_GLOBAL_INFO
title: PGET_GLOBAL_INFO
author: windows-driver-content
description: The GetGlobalInfo function retrieves global (as opposed to interface-specific) configuration information kept by the routing protocol.
old-location: rras\getglobalinfo.htm
old-project: RRAS
ms.assetid: 89d4ca42-8f78-40bd-96f0-ad10181cb2d4
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: GetGlobalInfo, GetGlobalInfo callback function [RAS], PGET_GLOBAL_INFO, PGET_GLOBAL_INFO callback, _mpr_getglobalinfo, routprot/GetGlobalInfo, rras.getglobalinfo
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
-	GetGlobalInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PGET_GLOBAL_INFO callback function


## -description


The 
<b>GetGlobalInfo</b> function retrieves global (as opposed to interface-specific) configuration information kept by the routing protocol.


## -parameters




### -param GlobalInfo [in]

Pointer to a buffer to receive the protocol-defined global configuration information. The format of this information is specific to the routing protocol.
					


### -param BufferSize


### -param StructureVersion


### -param StructureSize


### -param StructureCount








#### - GlobalInfoSize [in, out]

Pointer to a <b>DWORD</b> variable. 




On input this variable specifies the size, in bytes, of the buffer pointed to by the <i>GlobalInfo</i> parameter.

On output this variable receives the size, in bytes, of the data placed in the output buffer. If the initial size was not large enough, the variable contains the size required to hold all of the output data.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The routing protocol could not retrieve the global information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the output buffer provided is not large enough to hold the requested information. The required size is returned in the <b>DWORD</b> variable pointed to by <i>OutputDataSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>GlobalInfoSize</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/fd780458-ef23-4ef2-8fe8-29b32100917f">Routing Protocol Interface Functions</a>



<a href="https://msdn.microsoft.com/0429f5ca-6574-48f5-85ab-70b4677ca539">Routing Protocol Interface Reference</a>



<a href="https://msdn.microsoft.com/fd977a71-bfa7-40e4-9afc-4824989f857f">SetGlobalInfo</a>



<a href="https://msdn.microsoft.com/abcfa220-a860-48cc-92c5-60ce655678b7">SetInterfaceInfo</a>
 

 

