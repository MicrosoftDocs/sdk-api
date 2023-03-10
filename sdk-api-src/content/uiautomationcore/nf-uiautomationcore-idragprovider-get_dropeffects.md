---
UID: NF:uiautomationcore.IDragProvider.get_DropEffects
title: IDragProvider::get_DropEffects (uiautomationcore.h)
description: Retrieves an array of localized strings that enumerate the full set of effects that can happen when this element is dropped as part of a drag-and-drop operation.
helpviewer_keywords: ["DropEffects property [Windows Accessibility]","DropEffects property [Windows Accessibility]","IDragProvider interface","IDragProvider interface [Windows Accessibility]","DropEffects property","IDragProvider.DropEffects","IDragProvider.get_DropEffects","IDragProvider::DropEffects","IDragProvider::get_DropEffects","get_DropEffects","uiautomationcore/IDragProvider::DropEffects","uiautomationcore/IDragProvider::get_DropEffects","winauto.uiauto_idragprovider_dropeffects"]
old-location: winauto\uiauto_idragprovider_dropeffects.htm
tech.root: WinAuto
ms.assetid: 66DEC1A0-5AB4-41C7-AA7A-F512AE388999
ms.date: 12/05/2018
ms.keywords: DropEffects property [Windows Accessibility], DropEffects property [Windows Accessibility],IDragProvider interface, IDragProvider interface [Windows Accessibility],DropEffects property, IDragProvider.DropEffects, IDragProvider.get_DropEffects, IDragProvider::DropEffects, IDragProvider::get_DropEffects, get_DropEffects, uiautomationcore/IDragProvider::DropEffects, uiautomationcore/IDragProvider::get_DropEffects, winauto.uiauto_idragprovider_dropeffects
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IDragProvider::get_DropEffects
 - uiautomationcore/IDragProvider::get_DropEffects
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
 - IDragProvider.DropEffects
 - IDragProvider.get_DropEffects
---

# IDragProvider::get_DropEffects


## -description

Retrieves an array of localized strings that enumerate the  full set of effects that can happen when this element is dropped as part of a drag-and-drop operation.

This property is read-only.

## -parameters

## -remarks

Some drag operations support a set of different drop effects. For example, a drag operation initiated through a right-click might display a menu of options when the element is dropped.   In the source-only style of Microsoft UI Automation drag-and-drop, no elements implement the <a href="/windows/desktop/WinAuto/uiauto-implementingdroptarget">DropTarget</a> pattern.    To find out what effect dropping the dragged element will have, a client can query the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-idragprovider-get_dropeffect">DropEffect</a> property of the dragged element.  This property can be a short string such as "move", or a longer one, such as "insert into Main group".    The strings are always localized.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider">IDragProvider</a>