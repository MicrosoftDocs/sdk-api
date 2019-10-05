---
UID: NF:mprapi.MprAdminBufferFree
title: MprAdminBufferFree function (mprapi.h)
author: windows-sdk-content
description: The MprAdminBufferFree function frees memory buffers returned by _MprAdminDeviceEnum, MprAdminInterfaceGetInfo, MprAdminInterfaceDeviceGetInfo, MprAdminInterfaceEnum, MprAdminServerGetInfo, MprAdminInterfaceTransportGetInfo, and MprAdminTransportGetInfo.
old-location: rras\mpradminbufferfree.htm
tech.root: RRAS
ms.assetid: 60cae055-841a-4435-bf0e-4198b1ccdd4e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MprAdminBufferFree, MprAdminBufferFree function [RAS], _mpr_mpradminbufferfree, mprapi/MprAdminBufferFree, rras.mpradminbufferfree
ms.topic: function
f1_keywords: 
 - "mprapi/MprAdminBufferFree"
dev_langs:
 - c++
req.header: mprapi.h
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminBufferFree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminBufferFree function


## -description


The 
<b>MprAdminBufferFree</b> function frees memory buffers returned by: 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmindeviceenum">MprAdminDeviceEnum</a>, <a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetinfo">MprAdminInterfaceGetInfo</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacedevicegetinfo">MprAdminInterfaceDeviceGetInfo</a>, <a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfaceenum">MprAdminInterfaceEnum</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminservergetinfo">MprAdminServerGetInfo</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacetransportgetinfo">MprAdminInterfaceTransportGetInfo</a>, and 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmintransportgetinfo">MprAdminTransportGetInfo</a>.


## -parameters




### -param pBuffer [in]

Pointer to the memory buffer to free.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is the following error code.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfaceenum">MprAdminInterfaceEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetinfo">MprAdminInterfaceGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacetransportgetinfo">MprAdminInterfaceTransportGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminservergetinfo">MprAdminServerGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmintransportgetinfo">MprAdminTransportGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>
 

 

