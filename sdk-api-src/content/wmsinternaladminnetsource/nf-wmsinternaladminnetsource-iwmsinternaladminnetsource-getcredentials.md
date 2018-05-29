---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource.GetCredentials
title: IWMSInternalAdminNetSource::GetCredentials
author: windows-sdk-content
description: The GetCredentials method retrieves a cached password.
old-location: wmformat\iwmsinternaladminnetsource_getcredentials.htm
old-project: wmformat
ms.assetid: e4d6bcc3-a32b-4270-8b43-f3b6a5046fd6
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetCredentials, GetCredentials method [windows Media Format], GetCredentials method [windows Media Format],IWMSInternalAdminNetSource interface, IWMSInternalAdminNetSource interface [windows Media Format],GetCredentials method, IWMSInternalAdminNetSource.GetCredentials, IWMSInternalAdminNetSource::GetCredentials, IWMSInternalAdminNetSourceGetCredentials, wmformat.iwmsinternaladminnetsource_getcredentials, wmsinternaladminnetsource/IWMSInternalAdminNetSource::GetCredentials
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
req.typenames: NETSOURCE_URLCREDPOLICY_SETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMSInternalAdminNetSource.GetCredentials
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSInternalAdminNetSource::GetCredentials


## -description



The <b>GetCredentials</b> method retrieves a cached password.



This method has been superseded by <a href="https://msdn.microsoft.com/e351f403-4699-4666-b98f-2aed0b80e548">IWMSInternalAdminNetSource3::GetCredentialsEx2</a>. The methods of <b>IWMSInternalAdminNetSource3</b> are much more secure than the password caching methods in <b>IWMSInternalAdminNetSource</b> and should be used if available.


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




<a href="https://msdn.microsoft.com/0fbdad85-d94a-4598-bb25-f733df33692a">IWMSInternalAdminNetSource Interface</a>



<a href="https://msdn.microsoft.com/781b2868-c8e2-4d92-98f2-c2950fac3d9b">IWMSInternalAdminNetSource::GetCredentialFlags</a>



<a href="https://msdn.microsoft.com/c0655ed3-8d14-447a-b74f-054498eb75e9">IWMSInternalAdminNetSource::SetCredentials</a>
 

 

