---
UID: NF:mmc.IContextMenuProvider.AddPrimaryExtensionItems
title: IContextMenuProvider::AddPrimaryExtensionItems
author: windows-sdk-content
description: The IContextMenuProvider::AddPrimaryExtensionItems method enables one specific extension to add items to the insertion points defined for this context menu.
old-location: mmc\icontextmenuprovider_addprimaryextensionitems.htm
old-project: MMC
ms.assetid: 423106cd-3e81-4c4b-b28a-f7abc3bfe38b
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: AddPrimaryExtensionItems, AddPrimaryExtensionItems method [MMC], AddPrimaryExtensionItems method [MMC],IContextMenuProvider interface, IContextMenuProvider interface [MMC],AddPrimaryExtensionItems method, IContextMenuProvider.AddPrimaryExtensionItems, IContextMenuProvider::AddPrimaryExtensionItems, _slate_icontextmenuprovider_addprimaryextensionitems, mmc.icontextmenuprovider_addprimaryextensionitems, mmc/IContextMenuProvider::AddPrimaryExtensionItems
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IContextMenuProvider.AddPrimaryExtensionItems
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IContextMenuProvider::AddPrimaryExtensionItems


## -description


The <b>IContextMenuProvider::AddPrimaryExtensionItems</b> method enables one specific extension to add items to the insertion points defined for this context menu.


## -parameters




### -param piExtension [in]

A pointer to an 
<a href="_com_iunknown">IUnknown</a> interface on the object that implements the 
<a href="https://msdn.microsoft.com/8fa4434e-ccdc-43fb-877e-a6f6a5fc95b2">IExtendContextMenu</a> interface for the primary extension.


### -param piDataObject [in]

A pointer to the 
<a href="_ole_idataobject">IDataObject</a> interface on the object whose context menu is extended.


## -returns



Other values can be returned, depending on the implementation of 
<a href="https://msdn.microsoft.com/d4fc7bfd-b017-466e-81f2-74f13aec4b52">IExtendContextMenu::AddMenuItems</a> by the specified snap-in.




## -see-also




<a href="https://msdn.microsoft.com/141a650f-a829-47b1-abf9-427302d98444">IContextMenuCallback</a>



<a href="https://msdn.microsoft.com/3f9a5945-9b34-41fe-9c91-c782eb7eb739">IContextMenuProvider</a>



<a href="https://msdn.microsoft.com/8fa4434e-ccdc-43fb-877e-a6f6a5fc95b2">IExtendContextMenu</a>
 

 

