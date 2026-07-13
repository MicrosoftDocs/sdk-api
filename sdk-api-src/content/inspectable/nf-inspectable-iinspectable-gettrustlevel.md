---
UID: NF:inspectable.IInspectable.GetTrustLevel
title: IInspectable::GetTrustLevel (inspectable.h)
description: Gets the trust level of the current Windows Runtime object.
helpviewer_keywords: ["GetTrustLevel","GetTrustLevel method [Windows Runtime]","GetTrustLevel method [Windows Runtime]","IInputPaneInterop interface","GetTrustLevel method [Windows Runtime]","IInspectable interface","IInputPaneInterop interface [Windows Runtime]","GetTrustLevel method","IInputPaneInterop::GetTrustLevel","IInspectable interface [Windows Runtime]","GetTrustLevel method","IInspectable.GetTrustLevel","IInspectable::GetTrustLevel","inspectable/IInputPaneInterop::GetTrustLevel","inspectable/IInspectable::GetTrustLevel","winrt.iinspectable_gettrustlevel"]
old-location: winrt\iinspectable_gettrustlevel.htm
tech.root: WinRT
ms.assetid: E7E8AFD1-A8B7-4023-9F8B-573E0D2622F6
ms.date: 12/05/2018
ms.keywords: GetTrustLevel, GetTrustLevel method [Windows Runtime], GetTrustLevel method [Windows Runtime],IInputPaneInterop interface, GetTrustLevel method [Windows Runtime],IInspectable interface, IInputPaneInterop interface [Windows Runtime],GetTrustLevel method, IInputPaneInterop::GetTrustLevel, IInspectable interface [Windows Runtime],GetTrustLevel method, IInspectable.GetTrustLevel, IInspectable::GetTrustLevel, inspectable/IInputPaneInterop::GetTrustLevel, inspectable/IInspectable::GetTrustLevel, winrt.iinspectable_gettrustlevel
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
 - IInspectable::GetTrustLevel
 - inspectable/IInspectable::GetTrustLevel
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
 - IInspectable.GetTrustLevel
 - IInputPaneInterop.GetTrustLevel
---

## -description

Gets the trust level of the current Windows Runtime object.

## -parameters

### -param trustLevel [out]

Type: <b><a href="/windows/desktop/api/inspectable/ne-inspectable-trustlevel">TrustLevel</a>*</b>

The trust level of the current Windows Runtime object. The default is <b>BaseLevel</b>.

## -returns

Type: <b>HRESULT</b>

This method always returns <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/inputpaneinterop/nn-inputpaneinterop-iinputpaneinterop">IInputPaneInterop</a>

<a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>

[winrt::get_trust_level](/uwp/cpp-ref-for-winrt/get-trust-level)
