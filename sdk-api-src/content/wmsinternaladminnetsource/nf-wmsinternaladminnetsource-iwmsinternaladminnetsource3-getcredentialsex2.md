---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource3.GetCredentialsEx2
title: IWMSInternalAdminNetSource3::GetCredentialsEx2
author: windows-sdk-content
description: The GetCredentialsEx2 method retrieves a cached password. This improved version of IWMSInternalAdminNetSource2::GetCredentialsEx adds a flag (fClearTextAuthentication) that indicates whether credentials were sent in unencrypted form over the network.
old-location: wmformat\iwmsinternaladminnetsource3_getcredentialsex2.htm
old-project: wmformat
ms.assetid: e351f403-4699-4666-b98f-2aed0b80e548
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetCredentialsEx2, GetCredentialsEx2 method [windows Media Format], GetCredentialsEx2 method [windows Media Format],IWMSInternalAdminNetSource3 interface, IWMSInternalAdminNetSource3 interface [windows Media Format],GetCredentialsEx2 method, IWMSInternalAdminNetSource3.GetCredentialsEx2, IWMSInternalAdminNetSource3::GetCredentialsEx2, IWMSInternalAdminNetSource3GetCredentialsEx2, wmformat.iwmsinternaladminnetsource3_getcredentialsex2, wmsinternaladminnetsource/IWMSInternalAdminNetSource3::GetCredentialsEx2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsinternaladminnetsource.h
req.include-header: 
req.redist: 
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
 - IWMSInternalAdminNetSource3.GetCredentialsEx2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSInternalAdminNetSource3::GetCredentialsEx2


## -description



The <b>GetCredentialsEx2</b> method retrieves a cached password. This improved version of <b>IWMSInternalAdminNetSource2::GetCredentialsEx</b> adds a flag (<i>fClearTextAuthentication</i>) that indicates whether credentials were sent in unencrypted form over the network.




## -parameters




### -param bstrRealm [in]

String containing the realm name. Realm names are supplied by servers to distinguish different levels of access to their files. Not all servers have realm names, in which case the DNS name is used.

If <i>fProxy</i> is False, this realm refers to the host server. If <i>fProxy</i> is True, this realm refers to the proxy server.


### -param bstrUrl [in]

String containing the URL to which the credentials apply.


### -param fProxy [in]

Boolean value that is True if the password applies when using a proxy server to access the site specified by <i>bstrUrl</i>.


### -param fClearTextAuthentication [in]

Boolean value that is True if the cached credentials were previously sent over the network in an unencrypted form.


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




<a href="https://msdn.microsoft.com/b4ca08a4-6e2d-4646-b101-67bac67300b1">IWMSInternalAdminNetSource3 Interface</a>



<a href="https://msdn.microsoft.com/6d4fbd40-46f8-4f9e-b2bc-43c09acf4d67">IWMSInternalAdminNetSource3::SetCredentialsEx2</a>
 

 

