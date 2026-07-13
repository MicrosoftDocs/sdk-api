---
UID: NN:mbnapi.IMbnVendorSpecificOperation
title: IMbnVendorSpecificOperation (mbnapi.h)
description: Interface to pass requests from an application to the underlying Mobile Broadband miniport drivers.
helpviewer_keywords: ["IMbnVendorSpecificOperation","IMbnVendorSpecificOperation interface [Microsoft Broadband Networks]","IMbnVendorSpecificOperation interface [Microsoft Broadband Networks]","described","mbn.imbnvendorspecificoperation","mbnapi/IMbnVendorSpecificOperation"]
old-location: mbn\imbnvendorspecificoperation.htm
tech.root: mbn
ms.assetid: cbc905f6-c5ac-4c6a-9021-4ec00b938bb2
ms.date: 12/05/2018
ms.keywords: IMbnVendorSpecificOperation, IMbnVendorSpecificOperation interface [Microsoft Broadband Networks], IMbnVendorSpecificOperation interface [Microsoft Broadband Networks],described, mbn.imbnvendorspecificoperation, mbnapi/IMbnVendorSpecificOperation
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
 - IMbnVendorSpecificOperation
 - mbnapi/IMbnVendorSpecificOperation
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
 - IMbnVendorSpecificOperation
---

# IMbnVendorSpecificOperation interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Interface to pass requests from an application to the underlying Mobile Broadband miniport drivers.

## -inheritance

The <b>IMbnVendorSpecificOperation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnVendorSpecificOperation</b> also has these types of members:

## -remarks

The calling application can acquire this interface by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.
