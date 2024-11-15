---
UID: NF:uiautomationcore.IScrollProvider.Scroll
title: IScrollProvider::Scroll (uiautomationcore.h)
description: Scrolls the visible region of the content area horizontally and vertically. (IScrollProvider.Scroll)
helpviewer_keywords: ["IScrollProvider interface [Windows Accessibility]","Scroll method","IScrollProvider.Scroll","IScrollProvider::Scroll","Scroll","Scroll method [Windows Accessibility]","Scroll method [Windows Accessibility]","IScrollProvider interface","uiauto.uiauto_IScrollProvider_Scroll","uiauto_IScrollProvider_Scroll","uiautomationcore/IScrollProvider::Scroll","winauto.uiauto_IScrollProvider_Scroll"]
old-location: winauto\uiauto_IScrollProvider_Scroll.htm
tech.root: WinAuto
ms.assetid: d1bd15d2-beaf-4838-970a-00cfa2a7cfd9
ms.date: 12/05/2018
ms.keywords: IScrollProvider interface [Windows Accessibility],Scroll method, IScrollProvider.Scroll, IScrollProvider::Scroll, Scroll, Scroll method [Windows Accessibility], Scroll method [Windows Accessibility],IScrollProvider interface, uiauto.uiauto_IScrollProvider_Scroll, uiauto_IScrollProvider_Scroll, uiautomationcore/IScrollProvider::Scroll, winauto.uiauto_IScrollProvider_Scroll
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
 - IScrollProvider::Scroll
 - uiautomationcore/IScrollProvider::Scroll
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
 - IScrollProvider.Scroll
---

# IScrollProvider::Scroll


## -description

Scrolls the visible region of the content area horizontally and vertically.

## -parameters

### -param horizontalAmount [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-scrollamount">ScrollAmount</a></b>

The horizontal scrolling increment that is specific to the control.

### -param verticalAmount [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-scrollamount">ScrollAmount</a></b>

The vertical scrolling increment that is specific to the control.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iscrollprovider">IScrollProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
