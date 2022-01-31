---
UID: NE:uiribbon.UI_COLLECTIONCHANGE
title: UI_COLLECTIONCHANGE (uiribbon.h)
description: Specifies values that identify the types of changes that can be made to a collection.
helpviewer_keywords: ["UI_COLLECTIONCHANGE","UI_COLLECTIONCHANGE enumeration [Windows Ribbon]","UI_COLLECTIONCHANGE_INSERT","UI_COLLECTIONCHANGE_REMOVE","UI_COLLECTIONCHANGE_REPLACE","UI_COLLECTIONCHANGE_RESET","scenicintent_UI_COLLECTIONCHANGE","uiribbon/UI_COLLECTIONCHANGE","uiribbon/UI_COLLECTIONCHANGE_INSERT","uiribbon/UI_COLLECTIONCHANGE_REMOVE","uiribbon/UI_COLLECTIONCHANGE_REPLACE","uiribbon/UI_COLLECTIONCHANGE_RESET","windowsribbon.windowsribbon_ui_collectionchange"]
old-location: windowsribbon\windowsribbon_ui_collectionchange.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_collectionchange.htm
ms.date: 12/05/2018
ms.keywords: UI_COLLECTIONCHANGE, UI_COLLECTIONCHANGE enumeration [Windows Ribbon], UI_COLLECTIONCHANGE_INSERT, UI_COLLECTIONCHANGE_REMOVE, UI_COLLECTIONCHANGE_REPLACE, UI_COLLECTIONCHANGE_RESET, scenicintent_UI_COLLECTIONCHANGE, uiribbon/UI_COLLECTIONCHANGE, uiribbon/UI_COLLECTIONCHANGE_INSERT, uiribbon/UI_COLLECTIONCHANGE_REMOVE, uiribbon/UI_COLLECTIONCHANGE_REPLACE, uiribbon/UI_COLLECTIONCHANGE_RESET, windowsribbon.windowsribbon_ui_collectionchange
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UI_COLLECTIONCHANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UI_COLLECTIONCHANGE
 - uiribbon/UI_COLLECTIONCHANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_COLLECTIONCHANGE
---

# UI_COLLECTIONCHANGE enumeration


## -description

Specifies values that identify the types of changes that can be made to a collection.

## -enum-fields

### -field UI_COLLECTIONCHANGE_INSERT:0

Insert an item into the collection.

### -field UI_COLLECTIONCHANGE_REMOVE:1

Delete an item from the collection.

### -field UI_COLLECTIONCHANGE_REPLACE:2

Replace an item in the collection.

### -field UI_COLLECTIONCHANGE_RESET:3

Delete all items from the collection.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>



<a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged">IUICollectionChangedEvent::OnChanged</a>
