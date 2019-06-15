---
UID: NE:wmsdkidl.WMT_CREDENTIAL_FLAGS
title: WMT_CREDENTIAL_FLAGS (wmsdkidl.h)
author: windows-sdk-content
description: The WMT_CREDENTIAL_FLAGS enumeration type contains values used in the IWMCredentialCallback::AcquireCredentials method.
old-location: wmformat\wmt_credential_flags.htm
tech.root: wmformat
ms.assetid: a03e54e8-682d-4fbd-bd5c-38f58620d0d4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WMT_CREDENTIAL_CLEAR_TEXT, WMT_CREDENTIAL_DONT_CACHE, WMT_CREDENTIAL_ENCRYPT, WMT_CREDENTIAL_FLAGS, WMT_CREDENTIAL_FLAGS enumeration [windows Media Format], WMT_CREDENTIAL_PROXY, WMT_CREDENTIAL_SAVE, wmformat.wmt_credential_flags, wmsdkidl/WMT_CREDENTIAL_CLEAR_TEXT, wmsdkidl/WMT_CREDENTIAL_DONT_CACHE, wmsdkidl/WMT_CREDENTIAL_ENCRYPT, wmsdkidl/WMT_CREDENTIAL_FLAGS, wmsdkidl/WMT_CREDENTIAL_PROXY, wmsdkidl/WMT_CREDENTIAL_SAVE
ms.topic: enum
f1_keywords: ["wmsdkidl/WMT_CREDENTIAL_FLAGS"]
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_CREDENTIAL_FLAGS
product: Windows
targetos: Windows
req.typenames: WMT_CREDENTIAL_FLAGS
req.redist: 
ms.custom: 19H1
---

# WMT_CREDENTIAL_FLAGS enumeration


## -description



The <b>WMT_CREDENTIAL_FLAGS</b> enumeration type contains values used in the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials">IWMCredentialCallback::AcquireCredentials</a> method.




## -enum-fields




### -field WMT_CREDENTIAL_SAVE

The application can set this flag to indicate that the caller should save the credentials in a persistent manner.


### -field WMT_CREDENTIAL_DONT_CACHE

The application can set this flag to indicate that the caller should not cache the credentials in memory.


### -field WMT_CREDENTIAL_CLEAR_TEXT

If this flag is set when the <b>AcquireCredentials</b> method is called, it indicates that the credentials will be sent over the network unencrypted. Applications should not set this flag.


### -field WMT_CREDENTIAL_PROXY

If this flag is set when the <b>AcquireCredentials</b> method is called, it indicates that the credentials are for a proxy server. Applications should not set this flag.


### -field WMT_CREDENTIAL_ENCRYPT

If this flag is set when the <b>AcquireCredentials</b> method is called, it indicates that the caller can handle encrypted credentials. When this flag is set, the application has the option of encrypting the credentials. To encrypt the credentials, use the <b>CryptProtectData</b> function, which is described in the Platform SDK documentation. The application can also return the credentials in plain text. In that case, the caller automatically encrypts the credentials, unless the WMT_CREDENTIAL_CLEAR_TEXT flag was set when the <b>AcquireCredentials</b> method was called.

If the application encrypts the credentials, it must set the WMT_CREDENTIAL_ENCRYPT flag before the method returns. If the application returns the credentials in clear text, clear this flag before the method returns.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
 

 

