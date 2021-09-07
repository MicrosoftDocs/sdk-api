---
UID: NN:mswmdm.IComponentAuthenticate
title: IComponentAuthenticate (mswmdm.h)
description: The IComponentAuthenticate interface provides secure, encrypted communication between modules of Windows Media Device Manager.
helpviewer_keywords: ["IComponentAuthenticate","IComponentAuthenticate interface [windows Media Device Manager]","IComponentAuthenticate interface [windows Media Device Manager]","described","IComponentAuthenticateInterface","mswmdm/IComponentAuthenticate","wmdm.icomponentauthenticate"]
old-location: wmdm\icomponentauthenticate.htm
tech.root: WMDM
ms.assetid: 5da66dc2-825d-4332-b1cb-2b9d0fabb445
ms.date: 12/05/2018
ms.keywords: IComponentAuthenticate, IComponentAuthenticate interface [windows Media Device Manager], IComponentAuthenticate interface [windows Media Device Manager],described, IComponentAuthenticateInterface, mswmdm/IComponentAuthenticate, wmdm.icomponentauthenticate
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
 - IComponentAuthenticate
 - mswmdm/IComponentAuthenticate
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
 - IComponentAuthenticate
---

# IComponentAuthenticate interface


## -description

The <b>IComponentAuthenticate</b> interface provides secure, encrypted communication between modules of Windows Media Device Manager. It is implemented by a service provider and created and used by an application or plug-in. To get this interface, the application calls <b>CoCreateInstance</b> (__uuidof(MediaDevMgr)).

The application creates and passes this interface to <a href="/previous-versions/bb231595(v=vs.85)">CSecureChannelClient::SetInterface</a>, but never calls any methods on this interface.

The service provider implements the methods in this interface, and calls them on a private <a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer</a> member.

## -inheritance

The <b>IComponentAuthenticate</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComponentAuthenticate</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WMDM/authenticating-the-application">Authenticating the Application</a>



<a href="/windows/desktop/WMDM/authenticating-the-service-provider">Authenticating the Service Provider</a>



<a href="/windows/desktop/WMDM/interfaces-for-service-providers-and-applications">Interfaces for Service Providers and Applications</a>



<a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Using Secure Authenticated Channels</a>
