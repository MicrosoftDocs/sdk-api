---
UID: NF:mmc.IContextMenuProvider.AddThirdPartyExtensionItems
title: IContextMenuProvider::AddThirdPartyExtensionItems (mmc.h)
author: windows-sdk-content
description: The IContextMenuProvider::AddThirdPartyExtensionItems method enables third-party extensions to add items at specified insertion points in this context menu.
old-location: mmc\icontextmenuprovider_addthirdpartyextensionitems.htm
tech.root: mmc
ms.assetid: 8974b463-d4b6-464d-9bea-8d482d4804f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddThirdPartyExtensionItems, AddThirdPartyExtensionItems method [MMC], AddThirdPartyExtensionItems method [MMC],IContextMenuProvider interface, IContextMenuProvider interface [MMC],AddThirdPartyExtensionItems method, IContextMenuProvider.AddThirdPartyExtensionItems, IContextMenuProvider::AddThirdPartyExtensionItems, _slate_icontextmenuprovider_addthirdpartyextensionitems, mmc.icontextmenuprovider_addthirdpartyextensionitems, mmc/IContextMenuProvider::AddThirdPartyExtensionItems
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
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IContextMenuProvider.AddThirdPartyExtensionItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IContextMenuProvider::AddThirdPartyExtensionItems


## -description


The <b>IContextMenuProvider::AddThirdPartyExtensionItems</b> method enables third-party extensions to add items at specified insertion points in this context menu. MMC checks its list of snap-ins registered to extend objects of this node type and offers each (if there are any) the opportunity to extend the context menu by calling 
<a href="https://msdn.microsoft.com/d4fc7bfd-b017-466e-81f2-74f13aec4b52">IExtendContextMenu::AddMenuItems</a>.


## -parameters




### -param piDataObject [in]

A pointer to the 
<a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a> interface on the object whose menu is extended.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/141a650f-a829-47b1-abf9-427302d98444">IContextMenuCallback</a>



<a href="https://msdn.microsoft.com/3f9a5945-9b34-41fe-9c91-c782eb7eb739">IContextMenuProvider</a>



<a href="https://msdn.microsoft.com/8fa4434e-ccdc-43fb-877e-a6f6a5fc95b2">IExtendContextMenu</a>
 

 

