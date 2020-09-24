---
UID: NF:mprapi.MprAdminInterfaceGetCredentialsEx
title: MprAdminInterfaceGetCredentialsEx function (mprapi.h)
description: Use the MprAdminInterfaceGetCredentialsEx function to retrieve extended credentials information for the specified interface. Use this function to retrieve credentials information used for Extensible Authentication Protocols (EAPs).
helpviewer_keywords: ["MprAdminInterfaceGetCredentialsEx","MprAdminInterfaceGetCredentialsEx function [RAS]","_mpr_mpradmininterfacegetcredentialsex","mprapi/MprAdminInterfaceGetCredentialsEx","rras.mpradmininterfacegetcredentialsex"]
old-location: rras\mpradmininterfacegetcredentialsex.htm
tech.root: RRAS
ms.assetid: 0ef9f437-a15b-4f6c-ac76-4c31a23e8792
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceGetCredentialsEx, MprAdminInterfaceGetCredentialsEx function [RAS], _mpr_mpradmininterfacegetcredentialsex, mprapi/MprAdminInterfaceGetCredentialsEx, rras.mpradmininterfacegetcredentialsex
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
 - MprAdminInterfaceGetCredentialsEx
 - mprapi/MprAdminInterfaceGetCredentialsEx
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
 - MprAdminInterfaceGetCredentialsEx
---

# MprAdminInterfaceGetCredentialsEx function


## -description

Use the 
<b>MprAdminInterfaceGetCredentialsEx</b> function to retrieve extended credentials information for the specified interface. Use this function to retrieve credentials information used for Extensible Authentication Protocols (EAPs).

## -parameters

### -param hMprServer [in]

Handle to a router. This handle is obtained from a previous call to 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hInterface [in]

Handle to the interface. This handle is obtained from a previous call to 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpbBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0 or 1, as listed in the following table. 

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>Windows 2000 Server: <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_0">MPR_CREDENTIALSEX_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>Windows Server 2003 or later: <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_1">MPR_CREDENTIALSEX_1</a>
</td>
</tr>
</table>
 

A value of 1 indicates the information is a pre-shared key for the interface, which is in an encrypted format.

### -param lplpbBuffer [out]

On successful completion, a pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_0">MPR_CREDENTIALSEX_0</a> or <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_1">MPR_CREDENTIALSEX_1</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.
					Free the memory occupied by this structure with 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>.

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
The <i>lplpbBuffer</i> parameter is <b>NULL</b>.

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

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_0">MPR_CREDENTIALSEX_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_1">MPR_CREDENTIALSEX_1</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetcredentials">MprAdminInterfaceGetCredentials</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacesetcredentialsex">MprAdminInterfaceSetCredentialsEx</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>