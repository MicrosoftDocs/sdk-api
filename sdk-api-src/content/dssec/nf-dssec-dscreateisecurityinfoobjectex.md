---
UID: NF:dssec.DSCreateISecurityInfoObjectEx
title: DSCreateISecurityInfoObjectEx function
author: windows-sdk-content
description: Creates an instance of the ISecurityInformation interface associated with the specified directory service (DS) object on the specified server.
old-location: security\dscreateisecurityinfoobjectex.htm
tech.root: secauthz
ms.assetid: b0622c7b-49f2-4879-a0dc-9267851fe03d
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: DSCreateISecurityInfoObjectEx, DSCreateISecurityInfoObjectEx function [Security], DSSI_IS_ROOT, DSSI_NO_ACCESS_CHECK, DSSI_NO_EDIT_OWNER, DSSI_NO_EDIT_SACL, DSSI_NO_FILTER, DSSI_NO_READONLY_MESSAGE, DSSI_READ_ONLY, dssec/DSCreateISecurityInfoObjectEx, security.dscreateisecurityinfoobjectex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dssec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DSSec.lib
req.dll: DSSec.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DSSec.dll
api_name:
 - DSCreateISecurityInfoObjectEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DSCreateISecurityInfoObjectEx function


## -description


The <b>DSCreateISecurityInfoObjectEx</b> function creates an instance of the <a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a> interface associated with the specified directory service (DS) object on the specified server.


## -parameters




### -param pwszObjectPath [in]

The full path of the DS object for which to create an instance of the <a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a> interface.


### -param pwszObjectClass [in]

The class of the object specified by the <i>pwszObjectPath</i> parameter.


### -param pwszServer [in]

The server of the object specified by the <i>pwszObjectPath</i> parameter. If the value of this parameter is <b>NULL</b>, the server is obtained from the path specified by the <i>pwszObjectPath</i> parameter.


### -param pwszUserName [in]

A user name to be associated with the new <b>ISecurityInformation</b> object. If the value of this parameter is <b>NULL</b>, the <a href="https://msdn.microsoft.com/b24f9789-b9f5-49c4-9812-298bae8b28a9">Active Directory Services Interfaces</a> (ADSI) default is used.


### -param pwszPassword [in]

A password to be associated with the new <b>ISecurityInformation</b> object. If the value of this parameter is <b>NULL</b>, the <a href="https://msdn.microsoft.com/b24f9789-b9f5-49c4-9812-298bae8b28a9">Active Directory Services Interfaces</a> (ADSI) default is used.


### -param dwFlags [in]

Flags used for the security property page associated with the new instance of the <a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a> interface. This parameter can be any combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DSSI_READ_ONLY"></a><a id="dssi_read_only"></a><dl>
<dt><b>DSSI_READ_ONLY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The security properties are read-only.

</td>
</tr>
<tr>
<td width="40%"><a id="DSSI_NO_ACCESS_CHECK_"></a><a id="dssi_no_access_check_"></a><dl>
<dt><b>DSSI_NO_ACCESS_CHECK </b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
No access check is performed.

</td>
</tr>
<tr>
<td width="40%"><a id="DSSI_NO_EDIT_SACL"></a><a id="dssi_no_edit_sacl"></a><dl>
<dt><b>DSSI_NO_EDIT_SACL</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) property is read-only.

</td>
</tr>
<tr>
<td width="40%"><a id="DSSI_NO_EDIT_OWNER"></a><a id="dssi_no_edit_owner"></a><dl>
<dt><b>DSSI_NO_EDIT_OWNER</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The object owner property is read-only.

</td>
</tr>
<tr>
<td width="40%"><a id="DSSI_IS_ROOT"></a><a id="dssi_is_root"></a><dl>
<dt><b>DSSI_IS_ROOT</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The object is a root object.

</td>
</tr>
<tr>
<td width="40%"><a id="DSSI_NO_FILTER"></a><a id="dssi_no_filter"></a><dl>
<dt><b>DSSI_NO_FILTER</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Do not apply any filters.

</td>
</tr>
<tr>
<td width="40%"><a id="DSSI_NO_READONLY_MESSAGE"></a><a id="dssi_no_readonly_message"></a><dl>
<dt><b>DSSI_NO_READONLY_MESSAGE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Suppress read-only popup messages.

</td>
</tr>
</table>
 


### -param ppSI [out]

A pointer to the instance of the <a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a> interface this function creates.


### -param pfnReadSD [in, optional]

A pointer to a function used to read the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> of the object. This value can be <b>NULL</b>. If <i>pfnReadSD</i> is not <b>NULL</b>, <a href="https://msdn.microsoft.com/44cd8d55-7232-478a-a3d3-bbf5fc764bcd">DSCreateISecurityInfoObject</a>  calls the function referenced by <i>pfnReadSD</i> to retrieve the security descriptor of the object.


### -param pfnWriteSD [in, optional]

A pointer to  a function used to write the security descriptor of the object. This value can be <b>NULL</b>. If <i>pfnWriteSD</i> is not <b>NULL</b>, <a href="https://msdn.microsoft.com/44cd8d55-7232-478a-a3d3-bbf5fc764bcd">DSCreateISecurityInfoObject</a>  calls the function referenced by <i>pfnWriteSD</i> to write the security descriptor of the object.


### -param lpContext [in]

Context to pass to the functions identified by the <i>pfnReadSD</i> and <i>pfnWriteSD</i> parameters.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



