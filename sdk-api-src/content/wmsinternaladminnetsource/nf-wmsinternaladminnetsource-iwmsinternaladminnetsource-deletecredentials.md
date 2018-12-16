---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource.DeleteCredentials
title: IWMSInternalAdminNetSource::DeleteCredentials
author: windows-sdk-content
description: The DeleteCredentials method removes a password from the cache.
old-location: wmformat\iwmsinternaladminnetsource_deletecredentials.htm
tech.root: wmformat
ms.assetid: 16144c10-419c-4e6a-bc96-2f429c793257
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteCredentials, DeleteCredentials method [windows Media Format], DeleteCredentials method [windows Media Format],IWMSInternalAdminNetSource interface, IWMSInternalAdminNetSource interface [windows Media Format],DeleteCredentials method, IWMSInternalAdminNetSource.DeleteCredentials, IWMSInternalAdminNetSource::DeleteCredentials, IWMSInternalAdminNetSourceDeleteCredentials, wmformat.iwmsinternaladminnetsource_deletecredentials, wmsinternaladminnetsource/IWMSInternalAdminNetSource::DeleteCredentials
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
 - IWMSInternalAdminNetSource.DeleteCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSInternalAdminNetSource::DeleteCredentials


## -description



The <b>DeleteCredentials</b> method removes a password from the cache.



This method has been superseded by <a href="https://msdn.microsoft.com/en-us/library/Dd743719(v=VS.85).aspx">IWMSInternalAdminNetSource2::DeleteCredentialsEx</a>. The methods of <b>IWMSInternalAdminNetSource2</b> are much more secure than the password caching methods in <b>IWMSInternalAdminNetSource</b> and should be used if available.


## -parameters




### -param bstrRealm [in]

String containing the realm name. Realm names are supplied by servers to distinguish different levels of access to their files. Not all servers will have realm names, in which case the DNS name is used.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743717(v=VS.85).aspx">IWMSInternalAdminNetSource Interface</a>
 

 

