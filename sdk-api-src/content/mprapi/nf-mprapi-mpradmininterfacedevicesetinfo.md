---
UID: NF:mprapi.MprAdminInterfaceDeviceSetInfo
title: MprAdminInterfaceDeviceSetInfo function (mprapi.h)
description: The MprAdminInterfaceDeviceSetInfo creates or modifies a device that is used in a router demand-dial interface.
helpviewer_keywords: ["MprAdminInterfaceDeviceSetInfo","MprAdminInterfaceDeviceSetInfo function [RAS]","_mpr_mpradmininterfacedevicesetinfo","mprapi/MprAdminInterfaceDeviceSetInfo","rras.mpradmininterfacedevicesetinfo"]
old-location: rras\mpradmininterfacedevicesetinfo.htm
tech.root: RRAS
ms.assetid: ae8b3762-f176-4f91-97fc-33f7a9dcd424
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceDeviceSetInfo, MprAdminInterfaceDeviceSetInfo function [RAS], _mpr_mpradmininterfacedevicesetinfo, mprapi/MprAdminInterfaceDeviceSetInfo, rras.mpradmininterfacedevicesetinfo
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
 - MprAdminInterfaceDeviceSetInfo
 - mprapi/MprAdminInterfaceDeviceSetInfo
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
 - MprAdminInterfaceDeviceSetInfo
---

# MprAdminInterfaceDeviceSetInfo function


## -description

The 
<b>MprAdminInterfaceDeviceSetInfo</b> creates or modifies a device that is used in a router demand-dial interface.

## -parameters

### -param hMprServer [in]

Handle to the  router on which to execute this call. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hInterface [in]

Handle to the interface. Obtain this handle from a previous call to 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>, or by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfaceenum">MprAdminInterfaceEnum</a>.

### -param dwIndex [in]

Specifies the one-based index of the device. A multi-linked demand-dial interface uses multiple devices.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is structured in the <i>lplpBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0 or 1 as listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_device_0">MPR_DEVICE_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_device_1">MPR_DEVICE_1</a>
</td>
</tr>
</table>

### -param lpbBuffer [in]

A pointer to a <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_device_0">MPR_DEVICE_0</a> or <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_device_1">MPR_DEVICE_1</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling application does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hInterface</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lplpBuffer</i> parameter is <b>NULL</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwLevel</i> value is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_device_0">MPR_DEVICE_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_device_1">MPR_DEVICE_1</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacedevicegetinfo">MprAdminInterfaceDeviceGetInfo</a>