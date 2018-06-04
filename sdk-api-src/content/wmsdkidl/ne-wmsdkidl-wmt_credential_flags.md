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

# WMT_CREDENTIAL_FLAGS enumeration


## -description



The <b>WMT_CREDENTIAL_FLAGS</b> enumeration type contains values used in the <a href="https://msdn.microsoft.com/5dce8281-b5d3-42cd-93f6-d76af0050a89">IWMCredentialCallback::AcquireCredentials</a> method.




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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

