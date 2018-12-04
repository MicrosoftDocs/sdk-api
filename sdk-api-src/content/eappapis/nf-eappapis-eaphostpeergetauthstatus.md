---
UID: NF:eappapis.EapHostPeerGetAuthStatus
title: EapHostPeerGetAuthStatus function
author: windows-sdk-content
description: Obtains the supplicant's current EAP authentication status from EAPHost.
old-location: eaphost\eaphostpeergetauthstatus.htm
tech.root: eaphost
ms.assetid: cb5ceffb-941f-48ad-9271-111f41adc65b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EapHostNapInfo, EapHostPeerAuthStatus, EapHostPeerGetAuthStatus, EapHostPeerGetAuthStatus function [EAPHost], EapHostPeerIdentity, EapHostPeerIdentityExtendedInfo, eaphost.eaphostpeergetauthstatus, eappapis/EapHostPeerGetAuthStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: eappapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerGetAuthStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapHostPeerGetAuthStatus function


## -description


Obtains the supplicant's current EAP authentication status from EAPHost.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>.


### -param authParam [in]

An <a href="https://msdn.microsoft.com/adbb08d7-36a0-4e10-b0bc-2fb7030c2fcc">EapHostPeerAuthParams</a> enumeration value that specifies the type of EAP authentication data to obtain from EAPHost.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EapHostPeerAuthStatus"></a><a id="eaphostpeerauthstatus"></a><a id="EAPHOSTPEERAUTHSTATUS"></a><dl>
<dt><b>EapHostPeerAuthStatus</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAuthData</i> contains a <a href="https://msdn.microsoft.com/b05a1862-9709-4459-a445-5ea4e00cab88">EAPHOST_AUTH_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="EapHostPeerIdentity"></a><a id="eaphostpeeridentity"></a><a id="EAPHOSTPEERIDENTITY"></a><dl>
<dt><b>EapHostPeerIdentity</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAuthData</i> contains a <b>WCHAR</b> buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="EapHostPeerIdentityExtendedInfo"></a><a id="eaphostpeeridentityextendedinfo"></a><a id="EAPHOSTPEERIDENTITYEXTENDEDINFO"></a><dl>
<dt><b>EapHostPeerIdentityExtendedInfo</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAuthData</i> contains a <b>CHAR</b> buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="EapHostNapInfo"></a><a id="eaphostnapinfo"></a><a id="EAPHOSTNAPINFO"></a><dl>
<dt><b>EapHostNapInfo</b></dt>
</dl>
</td>
<td width="60%">
Windows 7 or later: <i>ppAuthData</i> contains a <a href="https://msdn.microsoft.com/703eda56-5932-44d5-ae7f-0a6328d82237">EapHostPeerNapInfo</a> structure.

</td>
</tr>
</table>
 


### -param pcbAuthData [out]

The size, in bytes, of the EAP authentication data buffer pointed to by the <i>ppAuthData</i> parameter. 


### -param ppAuthData [out]

A pointer to a pointer to a byte buffer that contains the authentication data from EAPHost. The format of this data depends on the value supplied in <i>authParam</i>. 


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeEapError</a>.


## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-Time Functions</a>
 

 

