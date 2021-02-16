---
UID: NF:mmc.IContextMenuProvider.AddThirdPartyExtensionItems
title: IContextMenuProvider::AddThirdPartyExtensionItems (mmc.h)
description: The IContextMenuProvider::AddThirdPartyExtensionItems method enables third-party extensions to add items at specified insertion points in this context menu.
helpviewer_keywords: ["AddThirdPartyExtensionItems","AddThirdPartyExtensionItems method [MMC]","AddThirdPartyExtensionItems method [MMC]","IContextMenuProvider interface","IContextMenuProvider interface [MMC]","AddThirdPartyExtensionItems method","IContextMenuProvider.AddThirdPartyExtensionItems","IContextMenuProvider::AddThirdPartyExtensionItems","_slate_icontextmenuprovider_addthirdpartyextensionitems","mmc.icontextmenuprovider_addthirdpartyextensionitems","mmc/IContextMenuProvider::AddThirdPartyExtensionItems"]
old-location: mmc\icontextmenuprovider_addthirdpartyextensionitems.htm
tech.root: mmc
ms.assetid: 8974b463-d4b6-464d-9bea-8d482d4804f3
ms.date: 12/05/2018
ms.keywords: AddThirdPartyExtensionItems, AddThirdPartyExtensionItems method [MMC], AddThirdPartyExtensionItems method [MMC],IContextMenuProvider interface, IContextMenuProvider interface [MMC],AddThirdPartyExtensionItems method, IContextMenuProvider.AddThirdPartyExtensionItems, IContextMenuProvider::AddThirdPartyExtensionItems, _slate_icontextmenuprovider_addthirdpartyextensionitems, mmc.icontextmenuprovider_addthirdpartyextensionitems, mmc/IContextMenuProvider::AddThirdPartyExtensionItems
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
 - IContextMenuProvider::AddThirdPartyExtensionItems
 - mmc/IContextMenuProvider::AddThirdPartyExtensionItems
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
 - IContextMenuProvider.AddThirdPartyExtensionItems
---

# IContextMenuProvider::AddThirdPartyExtensionItems


## -description

The <b>IContextMenuProvider::AddThirdPartyExtensionItems</b> method enables third-party extensions to add items at specified insertion points in this context menu. MMC checks its list of snap-ins registered to extend objects of this node type and offers each (if there are any) the opportunity to extend the context menu by calling 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendcontextmenu-addmenuitems">IExtendContextMenu::AddMenuItems</a>.

## -parameters

### -param piDataObject [in]

A pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the object whose menu is extended.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenucallback">IContextMenuCallback</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iextendcontextmenu">IExtendContextMenu</a>