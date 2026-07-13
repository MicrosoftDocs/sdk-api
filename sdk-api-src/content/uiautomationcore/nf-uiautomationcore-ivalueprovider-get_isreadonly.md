---
UID: NF:uiautomationcore.IValueProvider.get_IsReadOnly
title: IValueProvider::get_IsReadOnly (uiautomationcore.h)
description: Indicates whether the value of a control is read-only. (IValueProvider.get_IsReadOnly)
helpviewer_keywords: ["IValueProvider interface [Windows Accessibility]","IsReadOnly property","IValueProvider.IsReadOnly","IValueProvider.get_IsReadOnly","IValueProvider::IsReadOnly","IValueProvider::get_IsReadOnly","IsReadOnly property [Windows Accessibility]","IsReadOnly property [Windows Accessibility]","IValueProvider interface","get_IsReadOnly","uiauto.uiauto_IValueProvider_IsReadOnly","uiauto_IValueProvider_IsReadOnly","uiautomationcore/IValueProvider::IsReadOnly","uiautomationcore/IValueProvider::get_IsReadOnly","winauto.uiauto_IValueProvider_IsReadOnly"]
old-location: winauto\uiauto_IValueProvider_IsReadOnly.htm
tech.root: WinAuto
ms.assetid: 2dadeb17-aef8-4dcd-a2c5-251cc2e7de3f
ms.date: 12/05/2018
ms.keywords: IValueProvider interface [Windows Accessibility],IsReadOnly property, IValueProvider.IsReadOnly, IValueProvider.get_IsReadOnly, IValueProvider::IsReadOnly, IValueProvider::get_IsReadOnly, IsReadOnly property [Windows Accessibility], IsReadOnly property [Windows Accessibility],IValueProvider interface, get_IsReadOnly, uiauto.uiauto_IValueProvider_IsReadOnly, uiauto_IValueProvider_IsReadOnly, uiautomationcore/IValueProvider::IsReadOnly, uiautomationcore/IValueProvider::get_IsReadOnly, winauto.uiauto_IValueProvider_IsReadOnly
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
 - IValueProvider::get_IsReadOnly
 - uiautomationcore/IValueProvider::get_IsReadOnly
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
 - IValueProvider.IsReadOnly
 - IValueProvider.get_IsReadOnly
---

# IValueProvider::get_IsReadOnly


## -description

Indicates whether the value of a control is read-only. 

This property is read-only.

## -parameters

## -remarks

A control should have its IsEnabled property (<a href="/windows/desktop/WinAuto/uiauto-automation-element-propids">UIA_IsEnabledPropertyId</a>) set to <b>TRUE</b> and its <b>IValueProvider::IsReadOnly</b> 
            property set to <b>FALSE</b> before allowing a call to <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ivalueprovider-setvalue">IValueProvider::SetValue</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ivalueprovider">IValueProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
