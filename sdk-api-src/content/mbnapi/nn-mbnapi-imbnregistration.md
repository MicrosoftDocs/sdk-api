---
UID: NN:mbnapi.IMbnRegistration
title: IMbnRegistration (mbnapi.h)
description: Provides access to network registration data.
helpviewer_keywords: ["IMbnRegistration","IMbnRegistration interface [Microsoft Broadband Networks]","IMbnRegistration interface [Microsoft Broadband Networks]","described","mbn.imbnregistration","mbnapi/IMbnRegistration"]
old-location: mbn\imbnregistration.htm
tech.root: mbn
ms.assetid: da5413b7-adf4-4a3d-893f-f51441460541
ms.date: 12/05/2018
ms.keywords: IMbnRegistration, IMbnRegistration interface [Microsoft Broadband Networks], IMbnRegistration interface [Microsoft Broadband Networks],described, mbn.imbnregistration, mbnapi/IMbnRegistration
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
 - IMbnRegistration
 - mbnapi/IMbnRegistration
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
 - IMbnRegistration
---

# IMbnRegistration interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Provides access to network registration data.

## -inheritance

The <b>IMbnRegistration</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnRegistration</b> also has these types of members:

## -remarks

An application can acquire this interface by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.
