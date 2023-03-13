---
UID: NF:uiautomationcore.ITextRangeProvider.Select
title: ITextRangeProvider::Select (uiautomationcore.h)
description: Selects the span of text that corresponds to this text range, and removes any previous selection. (ITextRangeProvider.Select)
helpviewer_keywords: ["ITextRangeProvider interface [Windows Accessibility]","Select method","ITextRangeProvider.Select","ITextRangeProvider::Select","Select","Select method [Windows Accessibility]","Select method [Windows Accessibility]","ITextRangeProvider interface","uiauto.uiauto_ITextRangeProvider_Select","uiauto_ITextRangeProvider_Select","uiautomationcore/ITextRangeProvider::Select","winauto.uiauto_ITextRangeProvider_Select"]
old-location: winauto\uiauto_ITextRangeProvider_Select.htm
tech.root: WinAuto
ms.assetid: 486a604f-cea7-48de-aca2-2e9355699845
ms.date: 12/05/2018
ms.keywords: ITextRangeProvider interface [Windows Accessibility],Select method, ITextRangeProvider.Select, ITextRangeProvider::Select, Select, Select method [Windows Accessibility], Select method [Windows Accessibility],ITextRangeProvider interface, uiauto.uiauto_ITextRangeProvider_Select, uiauto_ITextRangeProvider_Select, uiautomationcore/ITextRangeProvider::Select, winauto.uiauto_ITextRangeProvider_Select
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
 - ITextRangeProvider::Select
 - uiautomationcore/ITextRangeProvider::Select
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
 - ITextRangeProvider.Select
---

# ITextRangeProvider::Select


## -description

Selects the span of text that corresponds to this text range, and removes any previous  selection.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Providing a degenerate text range will move the text insertion point.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
