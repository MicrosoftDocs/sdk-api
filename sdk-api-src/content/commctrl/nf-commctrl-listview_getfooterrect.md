---
UID: NF:commctrl.ListView_GetFooterRect
title: ListView_GetFooterRect macro
author: windows-sdk-content
description: Gets the coordinates of the footer for a specified list-view control. Use this macro or send the LVM_GETFOOTERRECT message explicitly.
old-location: controls\ListView_GetFooterRect.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getfooterrect.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ListView_GetFooterRect, ListView_GetFooterRect macro [Windows Controls], _shell_ListView_GetFooterRect, _shell_ListView_GetFooterRect_cpp, commctrl/ListView_GetFooterRect, controls.ListView_GetFooterRect, controls._shell_ListView_GetFooterRect
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
 - ListView_GetFooterRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetFooterRect macro


## -description


Gets the coordinates of the footer for a specified list-view control. Use this macro or send the <a href="https://msdn.microsoft.com/f8816f35-c1d2-4072-81d3-0a9a3df53d64">LVM_GETFOOTERRECT</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param prc [in, out]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure to receive the coordinates. The caller is responsible for allocating this structure. The coordinates received are expressed as client coordinates.

