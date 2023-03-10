---
UID: NN:mswmdm.ISCPSecureQuery
title: ISCPSecureQuery (mswmdm.h)
description: The ISCPSecureQuery interface is queried by Windows Media Device Manager to determine ownership of secured content.
helpviewer_keywords: ["ISCPSecureQuery","ISCPSecureQuery interface [windows Media Device Manager]","ISCPSecureQuery interface [windows Media Device Manager]","described","ISCPSecureQueryInterface","mswmdm/ISCPSecureQuery","wmdm.iscpsecurequery"]
old-location: wmdm\iscpsecurequery.htm
tech.root: WMDM
ms.assetid: d5f96629-26a1-4e83-a6a8-2d60c463f407
ms.date: 12/05/2018
ms.keywords: ISCPSecureQuery, ISCPSecureQuery interface [windows Media Device Manager], ISCPSecureQuery interface [windows Media Device Manager],described, ISCPSecureQueryInterface, mswmdm/ISCPSecureQuery, wmdm.iscpsecurequery
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
 - ISCPSecureQuery
 - mswmdm/ISCPSecureQuery
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
 - ISCPSecureQuery
---

# ISCPSecureQuery interface


## -description

The <b>ISCPSecureQuery</b> interface is queried by Windows Media Device Manager to determine ownership of secured content. Windows Media Device Manager passes information about the content to the secure content provider, which uses that information to determine whether it is responsible for the content. Windows Media Device Manager consults this interface whenever an application downloads content to a media device.

The <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2">ISCPSecureQuery2</a> interface extends <b>ISCPSecureQuery</b> through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.

The secure content provider implements this interface and secure Windows Media Device Manager implementations call its methods.

## -inheritance

The <b>ISCPSecureQuery</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISCPSecureQuery</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2">ISCPSecureQuery2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3">ISCPSecureQuery3 Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-secure-content-providers">Interfaces for Secure Content Providers</a>
