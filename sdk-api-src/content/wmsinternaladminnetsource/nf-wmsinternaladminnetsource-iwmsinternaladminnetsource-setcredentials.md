---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource.SetCredentials
title: IWMSInternalAdminNetSource::SetCredentials
author: windows-sdk-content
description: The SetCredentials method adds a password to the cache.
old-location: wmformat\iwmsinternaladminnetsource_setcredentials.htm
old-project: wmformat
ms.assetid: c0655ed3-8d14-447a-b74f-054498eb75e9
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWMSInternalAdminNetSource interface [windows Media Format],SetCredentials method, IWMSInternalAdminNetSource.SetCredentials, IWMSInternalAdminNetSource::SetCredentials, IWMSInternalAdminNetSourceSetCredentials, SetCredentials, SetCredentials method [windows Media Format], SetCredentials method [windows Media Format],IWMSInternalAdminNetSource interface, wmformat.iwmsinternaladminnetsource_setcredentials, wmsinternaladminnetsource/IWMSInternalAdminNetSource::SetCredentials
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
 - IWMSInternalAdminNetSource.SetCredentials
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSInternalAdminNetSource::SetCredentials


## -description



The <b>SetCredentials</b> method adds a password to the cache.



This method has been superseded by <a href="https://msdn.microsoft.com/6d4fbd40-46f8-4f9e-b2bc-43c09acf4d67">IWMSInternalAdminNetSource3::SetCredentialsEx2</a>. The methods of <b>IWMSInternalAdminNetSource3</b> are much more secure than the password caching methods in <b>IWMSInternalAdminNetSource</b> and should be used if available.


## -parameters




### -param bstrRealm [in]

String containing the realm name. Realm names are supplied by servers to distinguish different levels of access to their files. Not all servers have realm names, in which case the DNS name should be used.


### -param bstrName [in]

String containing the user name.


### -param bstrPassword [in]

String containing the password.


### -param fPersist [in]

Boolean value that is True if these credentials should be permanently saved. If you set this to False, the credentials will be saved only for the current session.


### -param fConfirmedGood [in]

Boolean value that is True if the server has confirmed the password as correct. You can cache the password before receiving verification from the server, in which case you should set this to False.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0fbdad85-d94a-4598-bb25-f733df33692a">IWMSInternalAdminNetSource Interface</a>



<a href="https://msdn.microsoft.com/e4d6bcc3-a32b-4270-8b43-f3b6a5046fd6">IWMSInternalAdminNetSource::GetCredentials</a>



<a href="https://msdn.microsoft.com/af6208b3-84f6-44d1-9587-140044f2b2f0">IWMSInternalAdminNetSource::SetCredentialFlags</a>
 

 

