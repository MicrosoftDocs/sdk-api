---
UID: NN:mswmdm.ISCPSecureAuthenticate
title: ISCPSecureAuthenticate (mswmdm.h)
description: The ISCPSecureAuthenticate interface is the primary interface of the secure content provider, which Windows Media Device Manager queries to authenticate the secure content provider and to be authenticated by the secure content provider.
helpviewer_keywords: ["ISCPSecureAuthenticate","ISCPSecureAuthenticate interface [windows Media Device Manager]","ISCPSecureAuthenticate interface [windows Media Device Manager]","described","ISCPSecureAuthenticateInterface","mswmdm/ISCPSecureAuthenticate","wmdm.iscpsecureauthenticate"]
old-location: wmdm\iscpsecureauthenticate.htm
tech.root: WMDM
ms.assetid: dfe37b41-f80b-4992-84c1-c23581cc4b69
ms.date: 12/05/2018
ms.keywords: ISCPSecureAuthenticate, ISCPSecureAuthenticate interface [windows Media Device Manager], ISCPSecureAuthenticate interface [windows Media Device Manager],described, ISCPSecureAuthenticateInterface, mswmdm/ISCPSecureAuthenticate, wmdm.iscpsecureauthenticate
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISCPSecureAuthenticate
 - mswmdm/ISCPSecureAuthenticate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - ISCPSecureAuthenticate
---

# ISCPSecureAuthenticate interface


## -description

The <b>ISCPSecureAuthenticate</b> interface is the primary interface of the secure content provider, which Windows Media Device Manager queries to authenticate the secure content provider and to be authenticated by the secure content provider. This interface is used to pass information about the content to the secure content provider module, which the provider uses to report back whether it is responsible for the content. Windows Media Device Manager consults this interface whenever an application downloads content to a media device.

The secure content provider implements this interface, and Windows Media Device Manager calls its methods.

## -inheritance

The <b>ISCPSecureAuthenticate</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISCPSecureAuthenticate</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-secure-content-providers">Interfaces for Secure Content Providers</a>
