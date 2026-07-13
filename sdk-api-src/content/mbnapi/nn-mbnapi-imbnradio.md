---
UID: NN:mbnapi.IMbnRadio
title: IMbnRadio (mbnapi.h)
description: The IMbnRadio interface is used to query and update the radio state of Mobile Broadband devices.
helpviewer_keywords: ["IMbnRadio","IMbnRadio interface [Microsoft Broadband Networks]","IMbnRadio interface [Microsoft Broadband Networks]","described","mbn.imbnradio","mbnapi/IMbnRadio"]
old-location: mbn\imbnradio.htm
tech.root: mbn
ms.assetid: b4b5ccfc-6cbf-4090-aee1-ee97092147f7
ms.date: 12/05/2018
ms.keywords: IMbnRadio, IMbnRadio interface [Microsoft Broadband Networks], IMbnRadio interface [Microsoft Broadband Networks],described, mbn.imbnradio, mbnapi/IMbnRadio
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
 - IMbnRadio
 - mbnapi/IMbnRadio
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
 - IMbnRadio
---

# IMbnRadio interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>IMbnRadio</b> interface is used to query and update the radio state of Mobile Broadband devices.

## -inheritance

The <b>IMbnRadio</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnRadio</b> also has these types of members:

## -remarks

An application can acquire this interface by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.
