---
UID: NF:uiautomationcore.ITextRangeProvider2.ShowContextMenu
title: ITextRangeProvider2::ShowContextMenu
author: windows-sdk-content
description: Programmatically invokes a context menu on the target element.
old-location: winauto\uiauto_ITextRangeProvider2_ShowContextMenu.htm
tech.root: WinAuto
ms.assetid: 7CE8B351-6103-1A73-8E74-7B21C90EC953
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextRangeProvider2 interface [Windows Accessibility],ShowContextMenu method, ITextRangeProvider2.ShowContextMenu, ITextRangeProvider2::ShowContextMenu, ShowContextMenu, ShowContextMenu method [Windows Accessibility], ShowContextMenu method [Windows Accessibility],ITextRangeProvider2 interface, uiautomationcore/ITextRangeProvider2::ShowContextMenu, winauto.uiauto_ITextRangeProvider2_ShowContextMenu
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextRangeProvider2.ShowContextMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRangeProvider2::ShowContextMenu


## -description


Programmatically invokes a context menu on the target element.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method should return an error code if the context menu could not be invoked.

<b>ShowContextMenu</b> should always show the context menu at the beginning end point of the range.  This should be equivalent to what would happen if the user pressed the context menu key or SHIFT + F10 with the insertion point at the beginning of the range.

If showing the context menu would typically result in the insertion point moving to a given location, then it should do so for programmatically invoking <b>ShowContextMenu</b> for Microsoft UI Automation support also.




## -see-also




<a href="https://msdn.microsoft.com/97A48D32-E8B2-31CB-2DC3-B9FDDF1BB3CC">ITextRangeProvider2</a>
 

 

