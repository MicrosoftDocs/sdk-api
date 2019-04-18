---
UID: NS:winsock2._WSANAMESPACE_INFOEXA
title: WSANAMESPACE_INFOEXA (winsock2.h)
author: windows-sdk-content
description: Contains all registration information for a namespace provider.
old-location: winsock\wsanamespace_infoex.htm
tech.root: WinSock
ms.assetid: 3f4a8916-9db9-4b65-982f-4cb4ec2205ed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPWSANAMESPACE_INFOEXA, *PWSANAMESPACE_INFOEXA, LPWSANAMESPACE_INFOEX, LPWSANAMESPACE_INFOEX structure pointer [Winsock], NS_BTH, NS_DNS, NS_EMAIL, NS_NLA, NS_NTDS, NS_PNRPCLOUD, NS_PNRPNAME, PWSANAMESPACE_INFOEX, PWSANAMESPACE_INFOEX structure pointer [Winsock], WSANAMESPACE_INFOEX, WSANAMESPACE_INFOEX structure [Winsock], WSANAMESPACE_INFOEXA, WSANAMESPACE_INFOEXW, winsock.wsanamespace_infoex, winsock2/LPWSANAMESPACE_INFOEX, winsock2/PWSANAMESPACE_INFOEX, winsock2/WSANAMESPACE_INFOEX, winsock2/WSANAMESPACE_INFOEXA, winsock2/WSANAMESPACE_INFOEXW"
ms.topic: struct
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSANAMESPACE_INFOEXW (Unicode) and WSANAMESPACE_INFOEXA (ANSI)
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
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - WSANAMESPACE_INFOEX
 - WSANAMESPACE_INFOEXA
 - WSANAMESPACE_INFOEXW
product: Windows
targetos: Windows
req.typenames: WSANAMESPACE_INFOEXA, *PWSANAMESPACE_INFOEXA, *LPWSANAMESPACE_INFOEXA
req.redist: 
ms.custom: 19H1
---

# WSANAMESPACE_INFOEXA structure


## -description


The 
<b>WSANAMESPACE_INFOEX</b> structure contains all registration information for a namespace provider.


## -struct-fields




### -field NSProviderId

Type: <b>GUID</b>

A unique GUID for this namespace provider.


### -field dwNameSpace

Type: <b>DWORD</b>

The namespace supported by this provider.


Possible values for the <b>dwNameSpace</b> member are listed in the <i>Winsock2.h</i> include file. Several namespace providers are included with Windows Vista and later. Other namespace providers can be installed, so the following possible values  are only those commonly available. Many other values are possible.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NS_BTH"></a><a id="ns_bth"></a><dl>
<dt><b>NS_BTH</b></dt>
</dl>
</td>
<td width="60%">
The Bluetooth namespace. 

This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_DNS"></a><a id="ns_dns"></a><dl>
<dt><b>NS_DNS</b></dt>
</dl>
</td>
<td width="60%">
The domain name system (DNS) namespace.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_EMAIL"></a><a id="ns_email"></a><dl>
<dt><b>NS_EMAIL</b></dt>
</dl>
</td>
<td width="60%">
The email namespace. 

This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NLA"></a><a id="ns_nla"></a><dl>
<dt><b>NS_NLA</b></dt>
</dl>
</td>
<td width="60%">
The network location awareness (NLA) namespace. 

This namespace identifier is supported on Windows XP and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NTDS"></a><a id="ns_ntds"></a><dl>
<dt><b>NS_NTDS</b></dt>
</dl>
</td>
<td width="60%">
The Windows NT directory service  (NTDS) namespace. 

</td>
</tr>
<tr>
<td width="40%"><a id="NS_PNRPNAME"></a><a id="ns_pnrpname"></a><dl>
<dt><b>NS_PNRPNAME</b></dt>
</dl>
</td>
<td width="60%">
The peer-to-peer name space for a specific peer name. 

This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_PNRPCLOUD"></a><a id="ns_pnrpcloud"></a><dl>
<dt><b>NS_PNRPCLOUD</b></dt>
</dl>
</td>
<td width="60%">
The peer-to-peer name space for a collection of peer names. 

This namespace identifier is supported on Windows Vista and later.

</td>
</tr>
</table>
 


### -field fActive

Type: <b>BOOL</b>

If <b>TRUE</b>, indicates that this namespace provider is active. If <b>FALSE</b>, the namespace provider is inactive and is not accessible for queries, even if the query specifically references this namespace provider.


### -field dwVersion

Type: <b>DWORD</b>

The version number of the namespace provider.


### -field lpszIdentifier

Type: <b>LPTSTR</b>

A display string that identifies the namespace provider.


### -field ProviderSpecific

Type: <b>BLOB</b>

A provider-specific data blob associated with namespace entry.


## -remarks



The <b>WSANAMESPACE_INFOEX</b>  structure is an enhanced version of the <a href="https://msdn.microsoft.com/a5c76657-df62-471a-95e9-8017cad47b00">WSANAMESPACE_INFO</a> structure that is used by the <a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a> and the <a href="https://msdn.microsoft.com/544120b2-7575-4deb-8429-2bd4582eceef">WSCEnumNameSpaceProvidersEx32</a> functions to return information on available namespace providers. The <b>WSANAMESPACE_INFOEX</b>  structure contains the provider-specific data blob associated with the namespace entry
                     passed in the <i>lpProviderInfo</i> parameter to the <a href="https://msdn.microsoft.com/13dde602-c958-4312-a16f-a393dd6fb829">WSCInstallNameSpaceEx</a> and <a href="https://msdn.microsoft.com/222ebfcc-8854-4224-b464-28098c84b750">WSCInstallNameSpaceEx32</a> functions.

  Currently, the only namespace included with Windows that uses information in the <b>ProviderSpecific</b> member of the <b>WSANAMESPACE_INFOEX</b> structure are namespace providers for the NS_EMAIL namespace. The format of the <b>ProviderSpecific</b> member for an NS_EMAIL namespace provider is a <a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure.

When UNICODE or _UNICODE is defined, <b>WSANAMESPACE_INFOEX</b> is defined to <b>WSANAMESPACE_INFOEXW</b>, the Unicode version of this structure and the <b>lpszIdentifier</b> string member is defined to the  <b>LPWSTR</b> data type.

When UNICODE or _UNICODE is not defined, <b>WSANAMESPACE_INFOEX</b> is defined to <b>WSANAMESPACE_INFOEXA</b>, the ANSI version of this structure and the <b>lpszIdentifier</b> string member is defined to the  <b>LPSTR</b> data type.

The <a href="https://msdn.microsoft.com/544120b2-7575-4deb-8429-2bd4582eceef">WSCEnumNameSpaceProvidersEx32</a> function is a Unicode only function and returns <b>WSANAMESPACE_INFOEXW</b> structures. 




## -see-also




<a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a>



<a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a>



<a href="https://msdn.microsoft.com/a5c76657-df62-471a-95e9-8017cad47b00">WSANAMESPACE_INFO</a>



<a href="https://msdn.microsoft.com/544120b2-7575-4deb-8429-2bd4582eceef">WSCEnumNameSpaceProvidersEx32</a>



<a href="https://msdn.microsoft.com/13dde602-c958-4312-a16f-a393dd6fb829">WSCInstallNameSpaceEx</a>



<a href="https://msdn.microsoft.com/222ebfcc-8854-4224-b464-28098c84b750">WSCInstallNameSpaceEx32</a>
 

 

