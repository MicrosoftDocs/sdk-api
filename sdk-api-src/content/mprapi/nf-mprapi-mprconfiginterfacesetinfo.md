---
UID: NF:mprapi.MprConfigInterfaceSetInfo
title: MprConfigInterfaceSetInfo function (mprapi.h)
description: The MprConfigInterfaceSetInfo function sets the configuration for the specified interface.
helpviewer_keywords: ["MprConfigInterfaceSetInfo","MprConfigInterfaceSetInfo function [RAS]","_mpr_mprconfiginterfacesetinfo","mprapi/MprConfigInterfaceSetInfo","rras.mprconfiginterfacesetinfo"]
old-location: rras\mprconfiginterfacesetinfo.htm
tech.root: RRAS
ms.assetid: 3abf3f27-a486-4b5c-a154-daf2dc99efaa
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceSetInfo, MprConfigInterfaceSetInfo function [RAS], _mpr_mprconfiginterfacesetinfo, mprapi/MprConfigInterfaceSetInfo, rras.mprconfiginterfacesetinfo
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
 - MprConfigInterfaceSetInfo
 - mprapi/MprConfigInterfaceSetInfo
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
 - MprConfigInterfaceSetInfo
---

# MprConfigInterfaceSetInfo function


## -description

The 
<b>MprConfigInterfaceSetInfo</b> function sets the configuration for the specified interface.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param hRouterInterface [in]

Handle to the interface configuration being updated. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>, 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>, or 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is structured in the <i>lpBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0, 1, 2, and 3, as listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>
</td>
</tr>
<tr>
<td>2</td>
<td>
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a>
</td>
</tr>
<tr>
<td>3</td>
<td>Windows Server 2008 or later: <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_3">MPR_INTERFACE_3</a>
</td>
</tr>
</table>

### -param lpbBuffer [in]

A pointer to a  
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a>, 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>,  
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a>, or  <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_3">MPR_INTERFACE_3</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.
					The information in this structure is used to update the interface configuration.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the following error codes.

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
At least one of the following is true:

<ul>
<li><i>hMprConfig</i> is <b>NULL</b>.</li>
<li><i>hRouterInterface</i> is <b>NULL</b>.</li>
<li><i>dwLevel</i> is not 0, 1, 2, or 3.</li>
<li><i>lpBuffer</i> is <b>NULL</b>.</li>
</ul>
Also returns this error code if the interface is of type <a href="/windows/desktop/api/mprapi/ne-mprapi-router_interface_type">ROUTER_IF_TYPE_DEDICATED</a> or <b>ROUTER_IF_TYPE_INTERNAL</b> and the interface is enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The interface that corresponds to <i>hRouterInterface</i> is not present in the router configuration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>

## -remarks

The 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacesetinfo">MprAdminInterfaceSetInfo</a> function supports the 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a> structure. However, 
<b>MprConfigInterfaceSetInfo</b> does not. In order to make persistent changes to a demand-dial interface, call 
<b>MprAdminInterfaceSetInfo</b> with 
<b>MPR_INTERFACE_2</b>, then call 
<b>MprConfigInterfaceSetInfo</b> with 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a> or 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacecreate">MprConfigInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegethandle">MprConfigInterfaceGetHandle</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>