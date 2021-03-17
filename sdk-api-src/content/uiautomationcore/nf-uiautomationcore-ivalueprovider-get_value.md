---
UID: NF:uiautomationcore.IValueProvider.get_Value
title: IValueProvider::get_Value (uiautomationcore.h)
description: The value of the control.
helpviewer_keywords: ["IValueProvider interface [Windows Accessibility]","Value property","IValueProvider.Value","IValueProvider.get_Value","IValueProvider::Value","IValueProvider::get_Value","Value property [Windows Accessibility]","Value property [Windows Accessibility]","IValueProvider interface","get_Value","uiauto.uiauto_IValueProvider_Value","uiauto_IValueProvider_Value","uiautomationcore/IValueProvider::Value","uiautomationcore/IValueProvider::get_Value","winauto.uiauto_IValueProvider_Value"]
old-location: winauto\uiauto_IValueProvider_Value.htm
tech.root: WinAuto
ms.assetid: 83cd0b99-32e4-4a25-aebb-b769745df78f
ms.date: 12/05/2018
ms.keywords: IValueProvider interface [Windows Accessibility],Value property, IValueProvider.Value, IValueProvider.get_Value, IValueProvider::Value, IValueProvider::get_Value, Value property [Windows Accessibility], Value property [Windows Accessibility],IValueProvider interface, get_Value, uiauto.uiauto_IValueProvider_Value, uiauto_IValueProvider_Value, uiautomationcore/IValueProvider::Value, uiautomationcore/IValueProvider::get_Value, winauto.uiauto_IValueProvider_Value
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
 - IValueProvider::get_Value
 - uiautomationcore/IValueProvider::get_Value
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
 - IValueProvider.Value
 - IValueProvider.get_Value
---

# IValueProvider::get_Value


## -description

The value of the control.

This property is read-only.

## -parameters

## -remarks

Single-line edit controls support programmatic access to their contents by implementing <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ivalueprovider">IValueProvider</a> (in addition to <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>). However, multi-line edit controls do not implement <b>IValueProvider</b>.


To retrieve the textual contents of multi-line edit controls, the controls must implement <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>. However, <b>ITextProvider</b> does not support setting the value of a control.



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ivalueprovider">IValueProvider</a> does not support the retrieval of formatting information or substring values. Implement <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a> in these scenarios.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ivalueprovider">IValueProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>