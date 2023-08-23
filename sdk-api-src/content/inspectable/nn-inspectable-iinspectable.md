---
UID: NN:inspectable.IInspectable
title: IInspectable (inspectable.h)
description: Provides functionality required for all Windows Runtime classes.
helpviewer_keywords: ["IInspectable","IInspectable interface [Windows Runtime]","IInspectable interface [Windows Runtime]","described","inspectable/IInspectable","winrt.iinspectable"]
old-location: winrt\iinspectable.htm
tech.root: WinRT
ms.assetid: 0657E51F-D4C0-46C6-927D-B01E54B6846C
ms.date: 12/05/2018
ms.keywords: IInspectable, IInspectable interface [Windows Runtime], IInspectable interface [Windows Runtime],described, inspectable/IInspectable, winrt.iinspectable
req.header: inspectable.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Inspectable.idl
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
 - IInspectable
 - inspectable/IInspectable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inspectable.h
api_name:
 - IInspectable
---

## -description

Provides functionality required for all Windows Runtime classes.

## -inheritance

The <b>IInspectable</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInspectable</b> also has these types of members:

## -remarks

<b>IInspectable</b> methods have no effect on COM apartments and are safe to call from user interface threads.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

<a href="/windows/desktop/api/inspectable/ne-inspectable-trustlevel">TrustLevel</a>

[winrt::get_interfaces](/uwp/cpp-ref-for-winrt/get-interfaces)

[winrt::get_class_name](/uwp/cpp-ref-for-winrt/get-class-name)

[winrt::get_trust_level](/uwp/cpp-ref-for-winrt/get-trust-level)
