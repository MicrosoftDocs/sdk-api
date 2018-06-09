---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource2.GetCredentialsEx
title: IWMSInternalAdminNetSource2::GetCredentialsEx
author: windows-sdk-content
description: The GetCredentialsEx method retrieves a cached password.
old-location: wmformat\iwmsinternaladminnetsource2_getcredentialsex.htm
old-project: wmformat
ms.assetid: 5840fe0b-34f6-4e39-b55f-7e07b7795e52
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetCredentialsEx, GetCredentialsEx method [windows Media Format], GetCredentialsEx method [windows Media Format],IWMSInternalAdminNetSource2 interface, IWMSInternalAdminNetSource2 interface [windows Media Format],GetCredentialsEx method, IWMSInternalAdminNetSource2.GetCredentialsEx, IWMSInternalAdminNetSource2::GetCredentialsEx, IWMSInternalAdminNetSource2GetCredentialsEx, wmformat.iwmsinternaladminnetsource2_getcredentialsex, wmsinternaladminnetsource/IWMSInternalAdminNetSource2::GetCredentialsEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsinternaladminnetsource.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
tech.root: 
req.typenames: NETSOURCE_URLCREDPOLICY_SETTINGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMSInternalAdminNetSource2.GetCredentialsEx
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSInternalAdminNetSource2::GetCredentialsEx


## -description



The <b>GetCredentialsEx</b> method retrieves a cached password. This improved version of <a href="https://msdn.microsoft.com/e4d6bcc3-a32b-4270-8b43-f3b6a5046fd6">IWMSInternalAdminNetSource::GetCredentials</a> uses the combination of realm, URL, and proxy use to identify the credentials. This is an improvement over using the realm by itself, which can easily be spoofed by malicious code.



This method has been superseded by <a href="https://msdn.microsoft.com/e351f403-4699-4666-b98f-2aed0b80e548">IWMSInternalAdminNetSource3::GetCredentialsEx2</a>.


## -parameters




### -param bstrRealm [in]

String containing the realm name. Realm names are supplied by servers to distinguish different levels of access to their files. Not all servers have realm names, in which case the DNS name is used.

If <i>fProxy</i> is False, this realm refers to the host server. If <i>fProxy</i> is True, this realm refers to the proxy server.


### -param bstrUrl [in]

String containing the URL to which the credentials apply.


### -param fProxy [in]

Boolean value that is True if the password applies when using a proxy server to access the site specified by <i>bstrUrl</i>.


### -param pdwUrlPolicy [out]

Pointer to a <b>DWORD</b> containing one member of the <a href="https://msdn.microsoft.com/d4ffdbc8-123e-4cb4-bcc9-8d52c3362529">NETSOURCE_URLCREDPOLICY_SETTINGS</a> enumeration type. This value is based on the user's network security settings and determines whether your application can automatically log in to sites for the user if you have credentials cached.


### -param pbstrName [out]

Pointer to a string containing the user name.


### -param pbstrPassword [out]

Pointer to a string containing the password.


### -param pfConfirmedGood [out]

Boolean value that is True if the password was cached after it was confirmed as correct by the server.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6d334725-11d5-4249-a83d-fc8c1c35a56f">IWMSInternalAdminNetSource2 Interface</a>



<a href="https://msdn.microsoft.com/ca45626e-3f4d-415d-a4d1-90ce0177bd10">IWMSInternalAdminNetSource2::SetCredentialsEx</a>
 

 

