---
UID: NF:mmc.IPropertySheetProvider.FindPropertySheet
title: IPropertySheetProvider::FindPropertySheet (mmc.h)
description: Determines whether a specific property sheet exists.
helpviewer_keywords: ["FindPropertySheet","FindPropertySheet method [MMC]","FindPropertySheet method [MMC]","IPropertySheetProvider interface","IPropertySheetProvider interface [MMC]","FindPropertySheet method","IPropertySheetProvider.FindPropertySheet","IPropertySheetProvider::FindPropertySheet","_slate_ipropertysheetprovider_findpropertysheet","mmc.ipropertysheetprovider_findpropertysheet","mmc/IPropertySheetProvider::FindPropertySheet"]
old-location: mmc\ipropertysheetprovider_findpropertysheet.htm
tech.root: mmc
ms.assetid: 14f3a2b7-9e14-4068-a85a-20c41d7e4a4d
ms.date: 12/05/2018
ms.keywords: FindPropertySheet, FindPropertySheet method [MMC], FindPropertySheet method [MMC],IPropertySheetProvider interface, IPropertySheetProvider interface [MMC],FindPropertySheet method, IPropertySheetProvider.FindPropertySheet, IPropertySheetProvider::FindPropertySheet, _slate_ipropertysheetprovider_findpropertysheet, mmc.ipropertysheetprovider_findpropertysheet, mmc/IPropertySheetProvider::FindPropertySheet
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertySheetProvider::FindPropertySheet
 - mmc/IPropertySheetProvider::FindPropertySheet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IPropertySheetProvider.FindPropertySheet
---

# IPropertySheetProvider::FindPropertySheet


## -description

The <b>IPropertySheetProvider::FindPropertySheet</b> method determines whether a specific property sheet exists.

## -parameters

### -param hItem

A handle to the selected item in the scope pane.

### -param lpComponent [in]

A pointer to the 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> interface on the selected object. <b>NULL</b> if the object selected is a folder (on the scope or result panes), and  
<b>IComponent</b> of the snap-in if it is a result pane leaf item.

### -param lpDataObject [in]

A pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the data object.

## -returns

This method can return one of these values.

## -remarks

Items in the scope pane are owned by the console so there is no need to interact with the 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a> interface. The snap-in must implement 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-compareobjects">IComponent::CompareObjects</a> or 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponentdata-compareobjects">IComponentData::CompareObjects</a> to compare the data object with other data objects for existing property sheets.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetprovider">IPropertySheetProvider</a>