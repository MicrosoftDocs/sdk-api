---
UID: NN:mswmdm.ISCPSecureQuery3
title: ISCPSecureQuery3 (mswmdm.h)
description: The ISCPSecureQuery3 interface extends ISCPSecureQuery2 by providing a set of new methods for retrieving the rights and making decision on a clear channel.
helpviewer_keywords: ["ISCPSecureQuery3","ISCPSecureQuery3 interface [windows Media Device Manager]","ISCPSecureQuery3 interface [windows Media Device Manager]","described","ISCPSecureQuery3Interface","mswmdm/ISCPSecureQuery3","wmdm.iscpsecurequery3"]
old-location: wmdm\iscpsecurequery3.htm
tech.root: WMDM
ms.assetid: 3d600ae9-5d5b-48f6-a162-e52f78beb983
ms.date: 12/05/2018
ms.keywords: ISCPSecureQuery3, ISCPSecureQuery3 interface [windows Media Device Manager], ISCPSecureQuery3 interface [windows Media Device Manager],described, ISCPSecureQuery3Interface, mswmdm/ISCPSecureQuery3, wmdm.iscpsecurequery3
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
 - ISCPSecureQuery3
 - mswmdm/ISCPSecureQuery3
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
 - ISCPSecureQuery3
---

# ISCPSecureQuery3 interface


## -description

The <b>ISCPSecureQuery3</b> interface extends <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2">ISCPSecureQuery2</a> by providing a set of new methods for retrieving the rights and making decision on a clear channel. These methods are more efficient because they do not involve encrypting and decrypting of parameters, which happens on a secure channel.

## -inheritance

The <b>ISCPSecureQuery3</b> interface inherits from <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2">ISCPSecureQuery2</a>. <b>ISCPSecureQuery3</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2">ISCPSecureQuery2 Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-secure-content-providers">Interfaces for Secure Content Providers</a>
