---
UID: NF:mprapi.MprAdminInterfaceSetCredentialsEx
title: MprAdminInterfaceSetCredentialsEx function (mprapi.h)
description: Use the MprAdminInterfaceSetCredentialsEx function to set extended credentials information for an interface. Use this function to set credentials information used for Extensible Authentication Protocols (EAPs).helpviewer_keywords: ["MprAdminInterfaceSetCredentialsEx","MprAdminInterfaceSetCredentialsEx function [RAS]","_mpr_mpradmininterfacesetcredentialsex","mprapi/MprAdminInterfaceSetCredentialsEx","rras.mpradmininterfacesetcredentialsex"]
old-location: rras\mpradmininterfacesetcredentialsex.htm
tech.root: RRAS
ms.assetid: d0807c03-3994-4624-97ea-94b55e7cd1e4
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceSetCredentialsEx, MprAdminInterfaceSetCredentialsEx function [RAS], _mpr_mpradmininterfacesetcredentialsex, mprapi/MprAdminInterfaceSetCredentialsEx, rras.mpradmininterfacesetcredentialsex
f1_keywords:
- mprapi/MprAdminInterfaceSetCredentialsEx
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
- MprAdminInterfaceSetCredentialsEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminInterfaceSetCredentialsEx function


## -description


Use the 
<b>MprAdminInterfaceSetCredentialsEx</b> function to set extended credentials information for an interface. Use this function to set credentials information used for Extensible Authentication Protocols (EAPs).


## -parameters




### -param hMprServer [in]

Handle to a  router. This handle is obtained from a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>. 


### -param hInterface [in]

Handle to the interface. This handle is obtained from a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>.


### -param dwLevel [in]

A DWORD value that describes the format in which the information is structured in the <i>lpbBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0 or 1 as listed in the following table. A value of 1 indicates the information is a pre-shared key for the interface.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>Windows 2000 Server: <a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_0">MPR_CREDENTIALSEX_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>Windows Server 2003 or later: <a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_1">MPR_CREDENTIALSEX_1</a>
</td>
</tr>
</table>
 


### -param lpbBuffer [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_0">MPR_CREDENTIALSEX_0</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_1">MPR_CREDENTIALSEX_1</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.


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
 




## -remarks



To a delete a pre-shared key, call 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacesetcredentials">MprAdminInterfaceSetCredentials</a> with the <b>dwSize</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_1">MPR_CREDENTIALSEX_1</a> structure set to zero.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_0">MPR_CREDENTIALSEX_0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_1">MPR_CREDENTIALSEX_1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacecreate">MprAdminInterfaceCreate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacesetcredentials">MprAdminInterfaceSetCredentials</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetcredentialsex">MprAdminInterfaceSetCredentialsEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>
 

 

