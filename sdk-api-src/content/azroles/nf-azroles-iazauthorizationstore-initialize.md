---
UID: NF:azroles.IAzAuthorizationStore.Initialize
title: IAzAuthorizationStore::Initialize (azroles.h)
description: Initializes the authorization manager.
helpviewer_keywords: ["AZ_AZSTORE_FLAG_AUDIT_IS_CRITICAL","AZ_AZSTORE_FLAG_BATCH_UPDATE","AZ_AZSTORE_FLAG_CREATE","AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY","AzAuthorizationStore object [Security]","Initialize method","IAzAuthorizationStore interface [Security]","Initialize method","IAzAuthorizationStore.Initialize","IAzAuthorizationStore::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","AzAuthorizationStore object","Initialize method [Security]","IAzAuthorizationStore interface","azroles/IAzAuthorizationStore::Initialize","security.azauthorizationstore_initialize"]
old-location: security\azauthorizationstore_initialize.htm
tech.root: security
ms.assetid: c461d50a-c785-4b32-b331-fe3a1693f4de
ms.date: 12/05/2018
ms.keywords: AZ_AZSTORE_FLAG_AUDIT_IS_CRITICAL, AZ_AZSTORE_FLAG_BATCH_UPDATE, AZ_AZSTORE_FLAG_CREATE, AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY, AzAuthorizationStore object [Security],Initialize method, IAzAuthorizationStore interface [Security],Initialize method, IAzAuthorizationStore.Initialize, IAzAuthorizationStore::Initialize, Initialize, Initialize method [Security], Initialize method [Security],AzAuthorizationStore object, Initialize method [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::Initialize, security.azauthorizationstore_initialize
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzAuthorizationStore::Initialize
 - azroles/IAzAuthorizationStore::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - AzAuthorizationStore.Initialize
 - IAzAuthorizationStore.Initialize
---

# IAzAuthorizationStore::Initialize


## -description

The <b>Initialize</b> method initializes the authorization manager.

## -parameters

### -param lFlags [in]

Flags that control the behavior of the initialization. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The authorization store is opened for use by the <b>Update</b> method and the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_AZSTORE_FLAG_AUDIT_IS_CRITICAL"></a><a id="az_azstore_flag_audit_is_critical"></a><dl>
<dt><b>AZ_AZSTORE_FLAG_AUDIT_IS_CRITICAL</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
The calling application is required to have SE_AUDIT_PRIVILEGE; if the application does not have the audit privilege, the <b>Initialize</b> method fails.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_AZSTORE_FLAG_BATCH_UPDATE"></a><a id="az_azstore_flag_batch_update"></a><dl>
<dt><b>AZ_AZSTORE_FLAG_BATCH_UPDATE</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
The provider is notified that many objects will be modified or created. The provider then optimizes submission of the changes for better performance. Use this flag only when multiple child objects of an <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object are updated  simultaneously, such as during an install or a controlled batch update.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_AZSTORE_FLAG_CREATE"></a><a id="az_azstore_flag_create"></a><dl>
<dt><b>AZ_AZSTORE_FLAG_CREATE</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
The system attempts to create the policy store specified by the <i>bstrPolicyURL</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY"></a><a id="az_azstore_flag_manage_store_only"></a><dl>
<dt><b>AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
An existing store is opened for management purposes. Run-time routines cannot  be performed.

</td>
</tr>
</table>
 

If the AZ_AZSTORE_FLAG_CREATE flag is specified:

<ul>
<li>The system will attempt to create the underlying policy store specified by the <i>bstrPolicyURL</i> parameter.</li>
<li>If the specified policy store exists, the <b>Initialize</b> method will fail with ERROR_ALREADY_EXISTS. </li>
<li>You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-submit">Submit</a> method to persist any changes made by this method.</li>
<li>The <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-updatecache">UpdateCache</a> method will fail until the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-submit">Submit</a> method is called. The underlying policy store is actually created when <b>Submit</b> is called.</li>
</ul>
If the AZ_AZSTORE_FLAG_CREATE flag is not specified, the system expects the underlying policy store to exist. If the store does not exist, the <b>Initialize</b> method will fail with ERROR_FILE_NOT_FOUND.

### -param bstrPolicyURL [in]

Location of the persistent copy of the authorization policy database.

This string must contain both the policy URL prefix and the provider-specific policy location. Authorization Manager uses the provider prefix to load the appropriate provider. The store is loaded from the provider-specific policy location. No spaces are allowed in the policy URL prefix.

The policy URL prefix for an Active Directory store is <b>msldap:</b>. The general format for the URL  is as follows:

<b>msldap://</b><i>ServerName</i><b>:</b><i>Port</i><b>//</b><i>DistinguishedNameForTheStore</i>

The server name and the port are optional. If a server name is not provided, the default domain controller is used. If a port is not specified, the default LDAP port (LDAP_PORT, 389) is used. The distinguished name (DN) for the store begins with the relative distinguished name (RDN) of the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object. For example, if the RDN of the <b>AzAuthorizationStore</b> object is MyStore and MyStore is in an organizational unit (OU) named AzMan, a possible URL for the Active Directory store is as follows:

msldap://<i>MyServer</i>/CN=MyStore,OU=AzMan,DC=<i>MyDomain</i>,DC=Fabrikam,DC=Com

The policy URL prefix for an XML store is <b>msxml:</b>.  The general format for an XML store URL is the same as for a file URL, as shown in the following examples:  


<ul>
<li>msxml://c:/abc/test.xml</li>
<li>msxml://\\server\share\abc.xml</li>
<li>msxml://d|/dir1/dir2/abc.xml</li>
<li>msxml://c:/Documents%20and%20Settings/test%2exml</li>
</ul>
Note that in the fourth example, the URL uses encoding for the space (%20) and the period (%2e) characters. Also, the traditional relative path notation is not supported in URLs. If you specify msxml://abc.xml, the URL points to the file at the root of your drive.

<div class="alert"><b>Note</b>  If an XML or SQL store is used over a network, the traffic is not automatically encrypted. IPsec can be used to encrypt the authorization information in transit. For an SQL store, it is also possible to set up the open database connectivity (ODBC) connection to use encryption. For information about how to set up the ODBC connection, see <a href="https://msdn.microsoft.com/library/aa198230.aspx">How to enable encryption after SQL Server has been installed (Network Utility)</a>.</div>
<div> </div>

### -param varReserved [in, optional]

Reserved for future use. This parameter can be one of the following values:

<ul>
<li>varReserved.vt == VT_ERROR and varReserved.scode == DISP_E_PARAMNOTFOUND</li>
<li>varReserved.vt == VT_EMPTY</li>
<li>varReserved.vt == VT_NULL</li>
<li>varReserved.vt == VT_I4 and varReserved.lVal == 0</li>
<li>varReserved.vt == VT_I2 and varReserved.iVal == 0</li>
</ul>

## -returns

 If the method succeeds, the method returns S_OK.

If the <i>bstrPolicyURL</i> parameter is not valid, the method returns HRESULT_FROM_WIN32(ERROR_INVALID_NAME).

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Active Directory supports Application Partitions, which are also known as Non-Domain Naming Contexts. These partitions are used as a location for programs to store application data. An Authorization Manager policy store cannot be created or kept in the Application Partition; instead, use the Program Data container as the container for Active Directory Authorization Manager policy stores.