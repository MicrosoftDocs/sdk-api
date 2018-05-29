---
UID: NS:winsock2._WSANAMESPACE_INFOW
title: "_WSANAMESPACE_INFOW"
author: windows-sdk-content
description: Contains all registration information for a namespace provider.
old-location: winsock\wsanamespace_info_2.htm
old-project: WinSock
ms.assetid: a5c76657-df62-471a-95e9-8017cad47b00
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: "*LPWSANAMESPACE_INFOW, *PWSANAMESPACE_INFOW, NS_BTH, NS_DNS, NS_EMAIL, NS_NLA, NS_NTDS, NS_PNRPCLOUD, NS_PNRPNAME, PWSANAMESPACE_INFO, PWSANAMESPACE_INFO structure pointer [Winsock], WSANAMESPACE_INFO, WSANAMESPACE_INFO structure [Winsock], WSANAMESPACE_INFOA, WSANAMESPACE_INFOW, _WSANAMESPACE_INFOW, _win32_wsanamespace_info_2, winsock.wsanamespace_info_2, winsock2/PWSANAMESPACE_INFO, winsock2/WSANAMESPACE_INFO, winsock2/WSANAMESPACE_INFOA, winsock2/WSANAMESPACE_INFOW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSANAMESPACE_INFOW (Unicode) and WSANAMESPACE_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSANAMESPACE_INFOW, *PWSANAMESPACE_INFOW, *LPWSANAMESPACE_INFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winsock2.h
api_name:
-	WSANAMESPACE_INFO
-	WSANAMESPACE_INFOA
-	WSANAMESPACE_INFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSANAMESPACE_INFOW structure


## -description



			The 
<b>WSANAMESPACE_INFO</b> structure contains all registration information for a namespace provider.


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


## -remarks



The <b>WSANAMESPACE_INFO</b> structure is used by the <a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a>
		and <a href="https://msdn.microsoft.com/792737d9-231d-4524-b1a6-b9904951d5b4">WSCEnumNameSpaceProviders32</a> functions to return information on available namespace providers. The <b>WSANAMESPACE_INFO</b>  structure contains the provider-specific information on the namespace entry
                     passed to the <a href="https://msdn.microsoft.com/f17f6174-879e-45e7-a250-975d1ee24fe0">WSCInstallNameSpace</a> and <a href="https://msdn.microsoft.com/b107fbe6-bbfb-45be-8419-4d85d3c4e80c">WSCInstallNameSpace32</a> functions when the namespace provider was installed.

When UNICODE or _UNICODE is defined, <b>WSANAMESPACE_INFO</b> is defined to <b>WSANAMESPACE_INFOW</b>, the Unicode version of this data structure and the <b>lpszIdentifier</b> string member is defined to the  <b>LPWSTR</b> data type.

When UNICODE or _UNICODE is not defined, <b>WSANAMESPACE_INFO</b> is defined to <b>WSANAMESPACE_INFOA</b>, the ANSI version of this data structure and the <b>lpszIdentifier</b> string member is defined to the  <b>LPSTR</b> data type.

On Windows Vista and later, <a href="https://msdn.microsoft.com/3f4a8916-9db9-4b65-982f-4cb4ec2205ed">WSANAMESPACE_INFOEX</a>, an enhanced version of the <b>WSANAMESPACE_INFO</b> structure, is returned by calls to the <a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a> and <a href="https://msdn.microsoft.com/544120b2-7575-4deb-8429-2bd4582eceef">WSCEnumNameSpaceProvidersEx32</a> functions




## -see-also




<a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a>



<a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a>



<a href="https://msdn.microsoft.com/3f4a8916-9db9-4b65-982f-4cb4ec2205ed">WSANAMESPACE_INFOEX</a>



<a href="https://msdn.microsoft.com/792737d9-231d-4524-b1a6-b9904951d5b4">WSCEnumNameSpaceProviders32</a>



<a href="https://msdn.microsoft.com/544120b2-7575-4deb-8429-2bd4582eceef">WSCEnumNameSpaceProvidersEx32</a>



<a href="https://msdn.microsoft.com/f17f6174-879e-45e7-a250-975d1ee24fe0">WSCInstallNameSpace</a>



<a href="https://msdn.microsoft.com/b107fbe6-bbfb-45be-8419-4d85d3c4e80c">WSCInstallNameSpace32</a>
 

 

