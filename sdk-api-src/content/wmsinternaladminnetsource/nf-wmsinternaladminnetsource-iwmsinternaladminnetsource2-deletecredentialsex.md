---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource2.DeleteCredentialsEx
title: IWMSInternalAdminNetSource2::DeleteCredentialsEx method
author: windows-driver-content
description: The DeleteCredentialsEx method removes a password from the cache.
old-location: wmformat\iwmsinternaladminnetsource2_deletecredentialsex.htm
old-project: wmformat
ms.assetid: 06d82f1d-b965-40fb-8a79-904ba5af7191
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: DeleteCredentialsEx method [windows Media Format], DeleteCredentialsEx method [windows Media Format], IWMSInternalAdminNetSource2 interface, DeleteCredentialsEx,IWMSInternalAdminNetSource2.DeleteCredentialsEx, IWMSInternalAdminNetSource2, IWMSInternalAdminNetSource2 interface [windows Media Format], DeleteCredentialsEx method, IWMSInternalAdminNetSource2::DeleteCredentialsEx, IWMSInternalAdminNetSource2DeleteCredentialsEx, wmformat.iwmsinternaladminnetsource2_deletecredentialsex, wmsinternaladminnetsource/IWMSInternalAdminNetSource2::DeleteCredentialsEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IWMSInternalAdminNetSource2.DeleteCredentialsEx
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSInternalAdminNetSource2::DeleteCredentialsEx method


## -description



The <b>DeleteCredentialsEx</b> method removes a password from the cache. This improved version of <a href="https://msdn.microsoft.com/16144c10-419c-4e6a-bc96-2f429c793257">IWMSInternalAdminNetSource::DeleteCredentials</a> uses the combination of realm, URL, and proxy use to identify the credentials. This is an improvement over using the realm by itself, which can easily be spoofed by malicious code.




## -parameters




### -param bstrRealm [in]

String containing the realm name. Realm names are supplied by servers to distinguish different levels of access to their files. Not all servers will have realm names, in which case the DNS name is used.


### -param bstrUrl [in]

String containing the URL to which the credentials apply.


### -param fProxy [in]

Boolean value that is True if the password applies when using a proxy server to access the site specified by <i>bstrUrl</i>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6d334725-11d5-4249-a83d-fc8c1c35a56f">IWMSInternalAdminNetSource2 Interface</a>
 

 

