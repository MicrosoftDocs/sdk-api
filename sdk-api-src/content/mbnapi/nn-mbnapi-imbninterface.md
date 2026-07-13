---
UID: NN:mbnapi.IMbnInterface
title: IMbnInterface (mbnapi.h)
description: Represents a Mobile Broadband device.
helpviewer_keywords: ["IMbnInterface","IMbnInterface interface [Microsoft Broadband Networks]","IMbnInterface interface [Microsoft Broadband Networks]","described","mbn.imbninterface","mbnapi/IMbnInterface"]
old-location: mbn\imbninterface.htm
tech.root: mbn
ms.assetid: 958bce42-4772-4706-8900-1f83c5d3d52b
ms.date: 12/05/2018
ms.keywords: IMbnInterface, IMbnInterface interface [Microsoft Broadband Networks], IMbnInterface interface [Microsoft Broadband Networks],described, mbn.imbninterface, mbnapi/IMbnInterface
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
 - IMbnInterface
 - mbnapi/IMbnInterface
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
 - IMbnInterface
---

# IMbnInterface interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Represents a Mobile Broadband device.

The properties and methods of <b>IMbnInterface</b> return the 
    state of the device. Applications should register for change event notifications by implementing 
    <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>.

## -inheritance

The <b>IMbnInterface</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnInterface</b> also has these types of members:

## -remarks

<b>IMbnInterface</b> objects are provided by calls to the 
     <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfacemanager-getinterface">GetInterface</a> and 
     <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfacemanager-getinterfaces">GetInterfaces</a> methods of the 
     <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager">IMbnInterfaceManager</a> interface.
