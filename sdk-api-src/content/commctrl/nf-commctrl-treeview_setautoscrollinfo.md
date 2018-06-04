---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



