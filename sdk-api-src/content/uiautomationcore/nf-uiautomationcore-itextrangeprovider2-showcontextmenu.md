---
UID: NF:uiautomationcore.ITextRangeProvider2.ShowContextMenu
title: ITextRangeProvider2::ShowContextMenu (uiautomationcore.h)
description: Programmatically invokes a context menu on the target element. (ITextRangeProvider2.ShowContextMenu)
helpviewer_keywords: ["ITextRangeProvider2 interface [Windows Accessibility]","ShowContextMenu method","ITextRangeProvider2.ShowContextMenu","ITextRangeProvider2::ShowContextMenu","ShowContextMenu","ShowContextMenu method [Windows Accessibility]","ShowContextMenu method [Windows Accessibility]","ITextRangeProvider2 interface","uiautomationcore/ITextRangeProvider2::ShowContextMenu","winauto.uiauto_ITextRangeProvider2_ShowContextMenu"]
old-location: winauto\uiauto_ITextRangeProvider2_ShowContextMenu.htm
tech.root: WinAuto
ms.assetid: 7CE8B351-6103-1A73-8E74-7B21C90EC953
ms.date: 12/05/2018
ms.keywords: ITextRangeProvider2 interface [Windows Accessibility],ShowContextMenu method, ITextRangeProvider2.ShowContextMenu, ITextRangeProvider2::ShowContextMenu, ShowContextMenu, ShowContextMenu method [Windows Accessibility], ShowContextMenu method [Windows Accessibility],ITextRangeProvider2 interface, uiautomationcore/ITextRangeProvider2::ShowContextMenu, winauto.uiauto_ITextRangeProvider2_ShowContextMenu
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - ITextRangeProvider2::ShowContextMenu
 - uiautomationcore/ITextRangeProvider2::ShowContextMenu
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
 - ITextRangeProvider2.ShowContextMenu
---

# ITextRangeProvider2::ShowContextMenu


## -description

Programmatically invokes a context menu on the target element.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method should return an error code if the context menu could not be invoked.

<b>ShowContextMenu</b> should always show the context menu at the beginning end point of the range.  This should be equivalent to what would happen if the user pressed the context menu key or SHIFT + F10 with the insertion point at the beginning of the range.

If showing the context menu would typically result in the insertion point moving to a given location, then it should do so for programmatically invoking <b>ShowContextMenu</b> for Microsoft UI Automation support also.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider2">ITextRangeProvider2</a>
