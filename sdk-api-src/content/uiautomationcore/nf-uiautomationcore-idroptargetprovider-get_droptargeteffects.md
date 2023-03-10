---
UID: NF:uiautomationcore.IDropTargetProvider.get_DropTargetEffects
title: IDropTargetProvider::get_DropTargetEffects (uiautomationcore.h)
description: Retrieves an array of localized strings that enumerate the full set of effects that can happen when the user drops a grabbed element on this drop target as part of a drag-and-drop operation. (IDropTargetProvider.get_DropTargetEffects)
helpviewer_keywords: ["DropTargetEffects property [Windows Accessibility]","DropTargetEffects property [Windows Accessibility]","IDropTargetProvider interface","IDropTargetProvider interface [Windows Accessibility]","DropTargetEffects property","IDropTargetProvider.DropTargetEffects","IDropTargetProvider.get_DropTargetEffects","IDropTargetProvider::DropTargetEffects","IDropTargetProvider::get_DropTargetEffects","get_DropTargetEffects","uiautomationcore/IDropTargetProvider::DropTargetEffects","uiautomationcore/IDropTargetProvider::get_DropTargetEffects","winauto.uiauto_idroptargetprovider_droptargeteffects"]
old-location: winauto\uiauto_idroptargetprovider_droptargeteffects.htm
tech.root: WinAuto
ms.assetid: FF4080DD-CED0-4F3C-9F0C-BB37BA94DC7D
ms.date: 12/05/2018
ms.keywords: DropTargetEffects property [Windows Accessibility], DropTargetEffects property [Windows Accessibility],IDropTargetProvider interface, IDropTargetProvider interface [Windows Accessibility],DropTargetEffects property, IDropTargetProvider.DropTargetEffects, IDropTargetProvider.get_DropTargetEffects, IDropTargetProvider::DropTargetEffects, IDropTargetProvider::get_DropTargetEffects, get_DropTargetEffects, uiautomationcore/IDropTargetProvider::DropTargetEffects, uiautomationcore/IDropTargetProvider::get_DropTargetEffects, winauto.uiauto_idroptargetprovider_droptargeteffects
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
 - IDropTargetProvider::get_DropTargetEffects
 - uiautomationcore/IDropTargetProvider::get_DropTargetEffects
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
 - IDropTargetProvider.DropTargetEffects
 - IDropTargetProvider.get_DropTargetEffects
---

# IDropTargetProvider::get_DropTargetEffects


## -description

Retrieves an array of localized strings that enumerate the full set of effects that can happen when the user drops a grabbed element on this drop target as part of a drag-and-drop operation.

This property is read-only.

## -parameters

## -remarks

Some drag operations support a set of different drop effects. For example, a drag operation that is initiated with a right-click might display a menu of options for the action that occurs when the element is dropped.  To find out the set of effects that can happen when the grabbed element is dropped, a client can query the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-idragprovider-get_dropeffects">DropEffects</a> property of the dragged element.  This property can contain short strings such as "move", or longer ones such as "insert into Main group".  The strings are always localized.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider">IDropTargetProvider</a>
