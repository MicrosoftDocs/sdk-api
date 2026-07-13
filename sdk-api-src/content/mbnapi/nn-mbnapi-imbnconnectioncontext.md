---
UID: NN:mbnapi.IMbnConnectionContext
title: IMbnConnectionContext (mbnapi.h)
description: Manages connection contexts.
helpviewer_keywords: ["IMbnConnectionContext","IMbnConnectionContext interface [Microsoft Broadband Networks]","IMbnConnectionContext interface [Microsoft Broadband Networks]","described","mbn.imbnconnectioncontext","mbnapi/IMbnConnectionContext"]
old-location: mbn\imbnconnectioncontext.htm
tech.root: mbn
ms.assetid: a9bc52dc-47f9-4b20-b98d-0287464a89e5
ms.date: 12/05/2018
ms.keywords: IMbnConnectionContext, IMbnConnectionContext interface [Microsoft Broadband Networks], IMbnConnectionContext interface [Microsoft Broadband Networks],described, mbn.imbnconnectioncontext, mbnapi/IMbnConnectionContext
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - IMbnConnectionContext
 - mbnapi/IMbnConnectionContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionContext
---

# IMbnConnectionContext interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Manages connection contexts.

A connection context is an abstraction of a specific set of network configuration parameters for setting up a virtual circuit or flow on top of the physical Mobile Broadband connection.

## -inheritance

The <b>IMbnConnectionContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnConnectionContext</b> also has these types of members:

## -remarks

An application can acquire this interface by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.
