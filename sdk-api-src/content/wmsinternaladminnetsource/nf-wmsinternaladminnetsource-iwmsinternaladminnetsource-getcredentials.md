---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource.GetCredentials
title: IWMSInternalAdminNetSource::GetCredentials (wmsinternaladminnetsource.h)
author: windows-sdk-content
description: The GetCredentials method retrieves a cached password.
old-location: wmformat\iwmsinternaladminnetsource_getcredentials.htm
tech.root: wmformat
ms.assetid: e4d6bcc3-a32b-4270-8b43-f3b6a5046fd6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCredentials, GetCredentials method [windows Media Format], GetCredentials method [windows Media Format],IWMSInternalAdminNetSource interface, IWMSInternalAdminNetSource interface [windows Media Format],GetCredentials method, IWMSInternalAdminNetSource.GetCredentials, IWMSInternalAdminNetSource::GetCredentials, IWMSInternalAdminNetSourceGetCredentials, wmformat.iwmsinternaladminnetsource_getcredentials, wmsinternaladminnetsource/IWMSInternalAdminNetSource::GetCredentials
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
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
 - IWMSInternalAdminNetSource.GetCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSInternalAdminNetSource::GetCredentials


## -description



The <b>GetCredentials</b> method retrieves a cached password.



This method has been superseded by <a href="https://msdn.microsoft.com/en-us/library/Dd743724(v=VS.85).aspx">IWMSInternalAdminNetSource3::GetCredentialsEx2</a>. The methods of <b>IWMSInternalAdminNetSource3</b> are much more secure than the password caching methods in <b>IWMSInternalAdminNetSource</b> and should be used if available.


## -parameters




### -param bstrRealm [in]

String containing the realm name. Realm names are supplied by servers to distinguish different levels of access to their files. Not all servers have realm names, in which case the DNS name is used.


### -param pbstrName [out]

Pointer to a string containing the user name.


### -param pbstrPassword [out]

Pointer to a string containing the password.


### -param pfConfirmedGood [out]

Pointer to a Boolean value that is set to True if the password was cached after it was confirmed as correct by the server.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743717(v=VS.85).aspx">IWMSInternalAdminNetSource Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798538(v=VS.85).aspx">IWMSInternalAdminNetSource::GetCredentialFlags</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798542(v=VS.85).aspx">IWMSInternalAdminNetSource::SetCredentials</a>
 

 

