---
UID: NC:routprot.PSET_GLOBAL_INFO
title: PSET_GLOBAL_INFO
author: windows-sdk-content
description: The SetGlobalInfo function sets the global (as opposed to interface-specific) configuration information kept by the routing protocol. The format of this information is specific to the routing protocol.
old-location: rras\setglobalinfo.htm
tech.root: rras
ms.assetid: fd977a71-bfa7-40e4-9afc-4824989f857f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: PSET_GLOBAL_INFO, PSET_GLOBAL_INFO callback, PSET_GLOBAL_INFO callback function [RAS], SetGlobalInfo, _mpr_setglobalinfo, routprot/PSET_GLOBAL_INFO, rras.setglobalinfo
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Routprot.h
api_name:
 - PSET_GLOBAL_INFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSET_GLOBAL_INFO callback function


## -description


The 
<b>SetGlobalInfo</b> function sets the global (as opposed to interface-specific) configuration information kept by the routing protocol. The format of this information is specific to the routing protocol.


## -parameters




### -param GlobalInfo [in]

Pointer to a buffer that specifies the protocol-defined global configuration information.


### -param StructureVersion


### -param StructureSize


### -param StructureCount








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
The routing protocol could not set the configuration information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>GlobalInfo</i> parameter is <b>NULL</b>, or one of the parameters in the configuration information is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/89d4ca42-8f78-40bd-96f0-ad10181cb2d4">GetGlobalInfo</a>



<a href="https://msdn.microsoft.com/ec662772-f864-4108-b676-3fa501b3b927">GetInterfaceInfo</a>



<a href="https://msdn.microsoft.com/fd780458-ef23-4ef2-8fe8-29b32100917f">Routing Protocol Interface Functions</a>



<a href="https://msdn.microsoft.com/0429f5ca-6574-48f5-85ab-70b4677ca539">Routing Protocol Interface Reference</a>
 

 

