---
UID: NF:uiautomationcore.ITextProvider.get_SupportedTextSelection
title: ITextProvider::get_SupportedTextSelection (uiautomationcore.h)
description: Retrieves a value that specifies the type of text selection that is supported by the control. (ITextProvider.get_SupportedTextSelection)
helpviewer_keywords: ["ITextProvider interface [Windows Accessibility]","SupportedTextSelection property","ITextProvider.SupportedTextSelection","ITextProvider.get_SupportedTextSelection","ITextProvider::SupportedTextSelection","ITextProvider::get_SupportedTextSelection","SupportedTextSelection property [Windows Accessibility]","SupportedTextSelection property [Windows Accessibility]","ITextProvider interface","get_SupportedTextSelection","uiauto.uiauto_ITextProvider_SupportedTextSelection","uiauto_ITextProvider_SupportedTextSelection","uiautomationcore/ITextProvider::SupportedTextSelection","uiautomationcore/ITextProvider::get_SupportedTextSelection","winauto.uiauto_ITextProvider_SupportedTextSelection"]
old-location: winauto\uiauto_ITextProvider_SupportedTextSelection.htm
tech.root: WinAuto
ms.assetid: a1f91515-2bc8-4560-850d-34c880c78c43
ms.date: 01/30/2020
ms.keywords: ITextProvider interface [Windows Accessibility],SupportedTextSelection property, ITextProvider.SupportedTextSelection, ITextProvider.get_SupportedTextSelection, ITextProvider::SupportedTextSelection, ITextProvider::get_SupportedTextSelection, SupportedTextSelection property [Windows Accessibility], SupportedTextSelection property [Windows Accessibility],ITextProvider interface, get_SupportedTextSelection, uiauto.uiauto_ITextProvider_SupportedTextSelection, uiauto_ITextProvider_SupportedTextSelection, uiautomationcore/ITextProvider::SupportedTextSelection, uiautomationcore/ITextProvider::get_SupportedTextSelection, winauto.uiauto_ITextProvider_SupportedTextSelection
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - ITextProvider::get_SupportedTextSelection
 - uiautomationcore/ITextProvider::get_SupportedTextSelection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextProvider.SupportedTextSelection
 - ITextProvider.get_SupportedTextSelection
---

# ITextProvider::get_SupportedTextSelection


## -description

Retrieves a value that specifies the type of text selection that is supported by the control.

This property is read-only.

## -parameters

*pRetVal*

Type: **[SupportedTextSelection](../uiautomationcore/ne-uiautomationcore-supportedtextselection.md)\***

When this function returns, contains a pointer to the [SupportedTextSelection](../uiautomationcore/ne-uiautomationcore-supportedtextselection.md) object.

## -syntax

```cpp
HRESULT get_SupportedTextSelection (SupportedTextSelection *pRetVal);
```

## -remarks

> ### Parameters
>
> `pRetVal` [out]
>
> Type: **[SupportedTextSelection](../uiautomationcore/ne-uiautomationcore-supportedtextselection.md)\***
>
> When this function returns, contains a pointer to the [SupportedTextSelection](../uiautomationcore/ne-uiautomationcore-supportedtextselection.md) object.

## -see-also

[ITextProvider interface](nn-uiautomationcore-itextprovider.md), [ITextRangeProvider interface](nn-uiautomationcore-itextrangeprovider.md), [UI Automation Providers Overview](/windows/desktop/WinAuto/uiauto-providersoverview)

