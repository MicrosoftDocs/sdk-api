---
UID: NF:identityprovider.IConnectedIdentityProvider.GetUrl
title: IConnectedIdentityProvider::GetUrl
author: windows-sdk-content
description: Returns the URL string for the specified wizard or webpage.
old-location: security\iconnectedidentityprovider_geturl.htm
old-project: secauthn
ms.assetid: 623A9AE8-D838-4F00-B81E-35031ADB67F5
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetUrl, GetUrl method [Security], GetUrl method [Security],IConnectedIdentityProvider interface, IConnectedIdentityProvider interface [Security],GetUrl method, IConnectedIdentityProvider.GetUrl, IConnectedIdentityProvider::GetUrl, identityprovider/IConnectedIdentityProvider::GetUrl, security.iconnectedidentityprovider_geturl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: identityprovider.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identityprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IDENTITY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identityprovider.h
api_name:
 - IConnectedIdentityProvider.GetUrl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IConnectedIdentityProvider::GetUrl


## -description


Returns the URL string for the specified wizard or webpage.


## -parameters




### -param Identifier [in]

Identifies the wizard or webpage that should be returned.


### -param Context [in]

Describes the context in which the URL will be displayed.


### -param PostData [out]

A <b>VARIANT</b> of type VT_ARRAY and VT_UI1 that will be posted to the provided URL. If the post data is not required, this parameter should be set to VT_EMPTY.


### -param Url [out]

Returns a URL for the specified identity wizard or webpage. The URL must begin with <b>https://</b>.


## -returns



If the method succeeds, the method returns S_OK.

If the method fails, the method returns a Win32 error code.




## -see-also




<a href="https://msdn.microsoft.com/0AF5036B-326E-4FBE-9F26-18F532EF0BB3">IConnectedIdentityProvider</a>
 

 

