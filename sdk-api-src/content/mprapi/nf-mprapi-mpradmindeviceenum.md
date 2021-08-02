---
UID: NF:mprapi.MprAdminDeviceEnum
title: MprAdminDeviceEnum function (mprapi.h)
description: Function is called to enumerate RAS capable devices installed on the computer that can return their name and type.
helpviewer_keywords: ["MprAdminDeviceEnum","MprAdminDeviceEnum function [RAS]","mprapi/MprAdminDeviceEnum","rras.mpradmindeviceenum"]
old-location: rras\mpradmindeviceenum.htm
tech.root: RRAS
ms.assetid: 092892fd-1b61-45c6-a05f-83fc193611b9
ms.date: 12/05/2018
ms.keywords: MprAdminDeviceEnum, MprAdminDeviceEnum function [RAS], mprapi/MprAdminDeviceEnum, rras.mpradmindeviceenum
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminDeviceEnum
 - mprapi/MprAdminDeviceEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminDeviceEnum
---

# MprAdminDeviceEnum function


## -description

The <b>MprAdminDeviceEnum</b> function is called to enumerate RAS capable devices installed on the computer that can return their name and type.

## -parameters

### -param hMprServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpbBuffer</i> parameter. Must be zero.

### -param lplpbBuffer [out]

On successful completion, an array of <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_device_0">MPR_DEVICE_0</a> structures that contains the RAS capable device information. Free this memory by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>.

### -param lpdwTotalEntries [out]

The number of entries of type <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_device_0">MPR_DEVICE_0</a> in <i>lplpbBuffer</i>.

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
<dt><b>ERROR_NOT_SUPPORTED </b></dt>
</dl>
</td>
<td width="60%">
The <i>dwlevel</i> parameter does not equal zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER </b></dt>
</dl>
</td>
<td width="60%">
The <i>lplpbBuffer</i> or <i>lpdwTotalEntries</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>