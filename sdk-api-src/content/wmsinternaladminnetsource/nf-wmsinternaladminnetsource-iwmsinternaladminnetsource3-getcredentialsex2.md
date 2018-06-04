---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

