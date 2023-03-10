---
UID: NN:mswmdm.ISCPSession
title: ISCPSession (mswmdm.h)
description: The ISCPSession interface provides efficient common state management for multiple operations.A secure content provider (SCP) session is useful when transferring multiple files.
helpviewer_keywords: ["ISCPSession","ISCPSession interface [windows Media Device Manager]","ISCPSession interface [windows Media Device Manager]","described","ISCPSessionInterface","mswmdm/ISCPSession","wmdm.iscpsession"]
old-location: wmdm\iscpsession.htm
tech.root: WMDM
ms.assetid: 4efd8e5a-490b-435b-b34d-7099198891b1
ms.date: 12/05/2018
ms.keywords: ISCPSession, ISCPSession interface [windows Media Device Manager], ISCPSession interface [windows Media Device Manager],described, ISCPSessionInterface, mswmdm/ISCPSession, wmdm.iscpsession
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
 - ISCPSession
 - mswmdm/ISCPSession
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
 - ISCPSession
---

# ISCPSession interface


## -description

The <b>ISCPSession</b> interface provides efficient common state management for multiple operations.

A secure content provider (SCP) session is useful when transferring multiple files. In that case, the session can help SCP do some of the operations only once instead of once for every file transfer. This results in better transfer performance.

## -inheritance

The <b>ISCPSession</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISCPSession</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WMDM/interfaces-for-secure-content-providers">Interfaces for Secure Content Providers</a>
