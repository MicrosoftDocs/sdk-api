---
UID: NF:mmc.IContextMenuProvider.AddPrimaryExtensionItems
title: IContextMenuProvider::AddPrimaryExtensionItems (mmc.h)
description: The IContextMenuProvider::AddPrimaryExtensionItems method enables one specific extension to add items to the insertion points defined for this context menu.
helpviewer_keywords: ["AddPrimaryExtensionItems","AddPrimaryExtensionItems method [MMC]","AddPrimaryExtensionItems method [MMC]","IContextMenuProvider interface","IContextMenuProvider interface [MMC]","AddPrimaryExtensionItems method","IContextMenuProvider.AddPrimaryExtensionItems","IContextMenuProvider::AddPrimaryExtensionItems","_slate_icontextmenuprovider_addprimaryextensionitems","mmc.icontextmenuprovider_addprimaryextensionitems","mmc/IContextMenuProvider::AddPrimaryExtensionItems"]
old-location: mmc\icontextmenuprovider_addprimaryextensionitems.htm
tech.root: mmc
ms.assetid: 423106cd-3e81-4c4b-b28a-f7abc3bfe38b
ms.date: 12/05/2018
ms.keywords: AddPrimaryExtensionItems, AddPrimaryExtensionItems method [MMC], AddPrimaryExtensionItems method [MMC],IContextMenuProvider interface, IContextMenuProvider interface [MMC],AddPrimaryExtensionItems method, IContextMenuProvider.AddPrimaryExtensionItems, IContextMenuProvider::AddPrimaryExtensionItems, _slate_icontextmenuprovider_addprimaryextensionitems, mmc.icontextmenuprovider_addprimaryextensionitems, mmc/IContextMenuProvider::AddPrimaryExtensionItems
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
 - IContextMenuProvider::AddPrimaryExtensionItems
 - mmc/IContextMenuProvider::AddPrimaryExtensionItems
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
 - IContextMenuProvider.AddPrimaryExtensionItems
---

# IContextMenuProvider::AddPrimaryExtensionItems


## -description

The <b>IContextMenuProvider::AddPrimaryExtensionItems</b> method enables one specific extension to add items to the insertion points defined for this context menu.

## -parameters

### -param piExtension [in]

A pointer to an 
<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the object that implements the 
<a href="/windows/desktop/api/mmc/nn-mmc-iextendcontextmenu">IExtendContextMenu</a> interface for the primary extension.

### -param piDataObject [in]

A pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the object whose context menu is extended.

## -returns

Other values can be returned, depending on the implementation of 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendcontextmenu-addmenuitems">IExtendContextMenu::AddMenuItems</a> by the specified snap-in.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenucallback">IContextMenuCallback</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iextendcontextmenu">IExtendContextMenu</a>