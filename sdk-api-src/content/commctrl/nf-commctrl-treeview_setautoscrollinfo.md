---
UID: NF:commctrl.TreeView_SetAutoScrollInfo
title: TreeView_SetAutoScrollInfo macro
author: windows-sdk-content
description: Sets information used to determine auto-scroll characteristics. Use this macro or send the TVM_SETAUTOSCROLLINFO message explicitly.
old-location: controls\TreeView_SetAutoScrollInfo.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setautoscrollinfo.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: TreeView_SetAutoScrollInfo, TreeView_SetAutoScrollInfo macro [Windows Controls], _shell_TreeView_SetAutoScrollInfo, _shell_TreeView_SetAutoScrollInfo_cpp, commctrl/TreeView_SetAutoScrollInfo, controls.TreeView_SetAutoScrollInfo, controls._shell_TreeView_SetAutoScrollInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - TreeView_SetAutoScrollInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeView_SetAutoScrollInfo macro


## -description


Sets information used to determine auto-scroll characteristics. Use this macro or send the <a href="https://msdn.microsoft.com/de55933f-1caa-4193-84de-0486c41e8f1f">TVM_SETAUTOSCROLLINFO</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param uPixPerSec

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies pixels per second. The offset to scroll is divided by the <i>uPixPerSec</i> to determine the total duration of the auto-scroll.


### -param uUpdateTime

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the redraw time interval. Redraw at every elasped interval, until the item is scrolled into view.  Given <i>uPixPerSec</i>, the location of the item is calculated and a repaint occurs. Set this value to create smooth scrolling.


## -remarks



Autoscroll information is used to scroll a nonvisible item into view. The control must have the <a href="Tree_View_Control_Window_Extended_Styles.htm">TVS_EX_AUTOHSCROLL</a> extended style. For information on extended styles, see Tree-View Control Extended Styles.



