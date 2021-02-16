---
UID: NF:uiautomationcore.IScrollProvider.get_VerticallyScrollable
title: IScrollProvider::get_VerticallyScrollable (uiautomationcore.h)
description: Indicates whether the control can scroll vertically.
helpviewer_keywords: ["IScrollProvider interface [Windows Accessibility]","VerticallyScrollable property","IScrollProvider.VerticallyScrollable","IScrollProvider.get_VerticallyScrollable","IScrollProvider::VerticallyScrollable","IScrollProvider::get_VerticallyScrollable","VerticallyScrollable property [Windows Accessibility]","VerticallyScrollable property [Windows Accessibility]","IScrollProvider interface","get_VerticallyScrollable","uiauto.uiauto_IScrollProvider_VerticallyScrollable","uiauto_IScrollProvider_VerticallyScrollable","uiautomationcore/IScrollProvider::VerticallyScrollable","uiautomationcore/IScrollProvider::get_VerticallyScrollable","winauto.uiauto_IScrollProvider_VerticallyScrollable"]
old-location: winauto\uiauto_IScrollProvider_VerticallyScrollable.htm
tech.root: WinAuto
ms.assetid: fadc0fd7-969c-4189-b37c-9b8243e30ac1
ms.date: 12/05/2018
ms.keywords: IScrollProvider interface [Windows Accessibility],VerticallyScrollable property, IScrollProvider.VerticallyScrollable, IScrollProvider.get_VerticallyScrollable, IScrollProvider::VerticallyScrollable, IScrollProvider::get_VerticallyScrollable, VerticallyScrollable property [Windows Accessibility], VerticallyScrollable property [Windows Accessibility],IScrollProvider interface, get_VerticallyScrollable, uiauto.uiauto_IScrollProvider_VerticallyScrollable, uiauto_IScrollProvider_VerticallyScrollable, uiautomationcore/IScrollProvider::VerticallyScrollable, uiautomationcore/IScrollProvider::get_VerticallyScrollable, winauto.uiauto_IScrollProvider_VerticallyScrollable
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
 - IScrollProvider::get_VerticallyScrollable
 - uiautomationcore/IScrollProvider::get_VerticallyScrollable
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
 - IScrollProvider.VerticallyScrollable
 - IScrollProvider.get_VerticallyScrollable
---

# IScrollProvider::get_VerticallyScrollable


## -description

Indicates whether the control can scroll vertically.
        

This property is read-only.

## -parameters

## -remarks

This property can be dynamic. For example, the content area of the control 
        might not be larger than the viewable area, meaning <b>IScrollProvider::VerticallyScrollable</b> 
        is <b>FALSE</b>. However, resizing the control or adding child items may increase the bounds of the 
        content area beyond the viewable area, meaning that <b>IScrollProvider::VerticallyScrollable</b> is <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iscrollprovider">IScrollProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>