---
UID: NN:mbnapi.IMbnPin
title: IMbnPin (mbnapi.h)
description: Represents the device PIN.
helpviewer_keywords: ["IMbnPin","IMbnPin interface [Microsoft Broadband Networks]","IMbnPin interface [Microsoft Broadband Networks]","described","mbn.imbnpin","mbnapi/IMbnPin"]
old-location: mbn\imbnpin.htm
tech.root: mbn
ms.assetid: 76764dbb-7de0-4b95-a210-60b8e6a4b24b
ms.date: 12/05/2018
ms.keywords: IMbnPin, IMbnPin interface [Microsoft Broadband Networks], IMbnPin interface [Microsoft Broadband Networks],described, mbn.imbnpin, mbnapi/IMbnPin
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
 - IMbnPin
 - mbnapi/IMbnPin
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
 - IMbnPin
---

# IMbnPin interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Represents the device PIN.

## -inheritance

The <b>IMbnPin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnPin</b> also has these types of members:

## -remarks

<b>IMbnPin</b> objects are provided by calls to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpin">GetPin</a> and <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpinlist">GetPinList</a> methods of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a> interface.
