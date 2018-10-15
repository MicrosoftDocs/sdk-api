---
UID: NF:commctrl.TreeView_SelectItem
title: TreeView_SelectItem macro
author: windows-sdk-content
description: Selects the specified tree-view item. You can use this macro or the TreeView_Select macro, or you can send the TVM_SELECTITEM message explicitly.
old-location: controls\TreeView_SelectItem.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_selectitem.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: TreeView_SelectItem, TreeView_SelectItem macro [Windows Controls], _win32_TreeView_SelectItem, _win32_TreeView_SelectItem_cpp, commctrl/TreeView_SelectItem, controls.TreeView_SelectItem, controls._win32_TreeView_SelectItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TreeView_SelectItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_SelectItem macro


## -description


Selects the specified tree-view item. You can use this macro or the <a href="https://msdn.microsoft.com/e23ef98b-7db7-4e61-aace-05e6520f8b5c">TreeView_Select</a> macro, or you can send the <a href="https://msdn.microsoft.com/8b943958-7b93-4e54-99de-200121cf0752">TVM_SELECTITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. If the <i>hitem</i> parameter is <b>NULL</b>, the control is set to have no selected item. 


## -remarks



When you call the <b>TreeView_SelectItem</b> macro, the control's parent window receives the <a href="https://msdn.microsoft.com/53f24ee0-433c-4680-9075-5e2b21117ed9">TVN_SELCHANGING</a> and <a href="https://msdn.microsoft.com/682170d3-5843-4d92-afeb-c37f3502ed5d">TVN_SELCHANGED</a> notification codes. Also, if the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item. In this case, the parent window receives the <a href="https://msdn.microsoft.com/5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec">TVN_ITEMEXPANDING</a> and <a href="https://msdn.microsoft.com/18d9d61d-6ec5-4d3b-9c02-36d0e61ed232">TVN_ITEMEXPANDED</a> notification codes. 

Using the <b>TreeView_SelectItem</b> macro is equivalent to sending the <a href="https://msdn.microsoft.com/8b943958-7b93-4e54-99de-200121cf0752">TVM_SELECTITEM</a> message with its <i>flag</i> parameter set to the TVGN_CARET value. 



