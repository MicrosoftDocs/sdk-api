---
UID: NF:commctrl.ListView_CancelEditLabel
title: ListView_CancelEditLabel macro
author: windows-sdk-content
description: Cancels an item text editing operation. You can use this macro or send the LVM_CANCELEDITLABEL message explicitly.
old-location: controls\ListView_CancelEditLabel.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_canceleditlabel.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListView_CancelEditLabel, ListView_CancelEditLabel macro [Windows Controls], _win32_ListView_CancelEditLabel, _win32_ListView_CancelEditLabel_cpp, commctrl/ListView_CancelEditLabel, controls.ListView_CancelEditLabel, controls._win32_ListView_CancelEditLabel
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_CancelEditLabel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_CancelEditLabel macro


## -description


Cancels an item text editing operation. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774886(v=VS.85).aspx">LVM_CANCELEDITLABEL</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



To use <b>ListView_CancelEditLabel</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



