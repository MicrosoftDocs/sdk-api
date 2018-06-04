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

# IWSManConnectionOptionsEx2::SetProxy


## -description


Sets the proxy information for the session.


## -parameters




### -param accessType [in]

Specifies the proxy access type. This parameter must be set to one of the values in the <a href="https://msdn.microsoft.com/c17c3600-6a19-4937-90ff-1a4f7cf5b123">WSManProxyAccessTypeFlags</a> enumeration. The default value is <b>WSManProxyWinHttpConfig</b>.


### -param authenticationMechanism [in]

Specifies the authentication mechanism to use for the proxy.  This parameter is optional and the default value is 0. If this parameter is set to 0, the WinRM client chooses either Kerberos or Negotiate. Otherwise, this parameter must be set to one of the values in the <a href="https://msdn.microsoft.com/4a86dfae-18c9-4865-8b8b-bb0ac01f558c">WSManProxyAuthenticationFlags</a> enumeration. The default value from the enumeration is <b>WSManFlagProxyAuthenticationUseNegotiate</b>.


### -param userName [in]

Specifies the user name for proxy authentication. This parameter is optional. If a value is not specified for this parameter, the default credentials are used.


### -param password [in]

Specifies the password for proxy authentication. This parameter is optional. If a value is not specified for this parameter, the default credentials are used.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The default credentials are the credentials under which the current thread is operating.




## -see-also




<a href="https://msdn.microsoft.com/09159904-0160-411d-af54-f6aca94d4d7d">IWSManConnectionOptionsEx2</a>
 

 

