---
UID: NF:uiautomationcore.IVirtualizedItemProvider.Realize
title: IVirtualizedItemProvider::Realize (uiautomationcore.h)
description: Makes the virtual item fully accessible as a UI Automation element. (IVirtualizedItemProvider.Realize)
helpviewer_keywords: ["IVirtualizedItemProvider interface [Windows Accessibility]","Realize method","IVirtualizedItemProvider.Realize","IVirtualizedItemProvider::Realize","Realize","Realize method [Windows Accessibility]","Realize method [Windows Accessibility]","IVirtualizedItemProvider interface","uiauto.uiauto_IVirtualizedItemProvider_Realize","uiauto_IVirtualizedItemProvider_Realize","uiautomationcore/IVirtualizedItemProvider::Realize","winauto.uiauto_IVirtualizedItemProvider_Realize"]
old-location: winauto\uiauto_IVirtualizedItemProvider_Realize.htm
tech.root: WinAuto
ms.assetid: ec69f0d2-a643-4f1b-892a-0d90f79afe72
ms.date: 12/05/2018
ms.keywords: IVirtualizedItemProvider interface [Windows Accessibility],Realize method, IVirtualizedItemProvider.Realize, IVirtualizedItemProvider::Realize, Realize, Realize method [Windows Accessibility], Realize method [Windows Accessibility],IVirtualizedItemProvider interface, uiauto.uiauto_IVirtualizedItemProvider_Realize, uiauto_IVirtualizedItemProvider_Realize, uiautomationcore/IVirtualizedItemProvider::Realize, winauto.uiauto_IVirtualizedItemProvider_Realize
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IVirtualizedItemProvider::Realize
 - uiautomationcore/IVirtualizedItemProvider::Realize
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
 - IVirtualizedItemProvider.Realize
---

# IVirtualizedItemProvider::Realize


## -description

Makes the virtual item fully accessible as a UI Automation element.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When an item is obtained from a virtual list, it is only a placeholder. Use this method to convert it to a full reference to UI Automation element.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ivirtualizeditemprovider">IVirtualizedItemProvider</a>
