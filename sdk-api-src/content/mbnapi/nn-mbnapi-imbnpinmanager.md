---
UID: NN:mbnapi.IMbnPinManager
title: IMbnPinManager (mbnapi.h)
description: Provides important details about the device PIN.
helpviewer_keywords: ["IMbnPinManager","IMbnPinManager interface [Microsoft Broadband Networks]","IMbnPinManager interface [Microsoft Broadband Networks]","described","mbn.imbnpinmanager","mbnapi/IMbnPinManager"]
old-location: mbn\imbnpinmanager.htm
tech.root: mbn
ms.assetid: b5cfabc7-81f8-4ea0-b6f4-5de011320f0b
ms.date: 12/05/2018
ms.keywords: IMbnPinManager, IMbnPinManager interface [Microsoft Broadband Networks], IMbnPinManager interface [Microsoft Broadband Networks],described, mbn.imbnpinmanager, mbnapi/IMbnPinManager
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
 - IMbnPinManager
 - mbnapi/IMbnPinManager
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
 - IMbnPinManager
---

# IMbnPinManager interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Provides important details about the device PIN.

## -inheritance

The <b>IMbnPinManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnPinManager</b> also has these types of members:

## -remarks

An application can acquire this interface by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.
