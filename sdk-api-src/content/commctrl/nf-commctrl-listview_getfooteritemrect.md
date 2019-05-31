---
UID: NF:commctrl.ListView_GetFooterItemRect
title: ListView_GetFooterItemRect macro (commctrl.h)
author: windows-sdk-content
description: Gets the coordinates of a footer for a specified item in a list-view control. Use this macro or send the LVM_GETFOOTERITEMRECT message explicitly.
old-location: controls\ListView_GetFooterItemRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getfooteritemrect.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_GetFooterItemRect, ListView_GetFooterItemRect macro [Windows Controls], _shell_ListView_GetFooterItemRect, _shell_ListView_GetFooterItemRect_cpp, commctrl/ListView_GetFooterItemRect, controls.ListView_GetFooterItemRect, controls._shell_ListView_GetFooterItemRect
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
 - ListView_GetFooterItemRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_GetFooterItemRect macro


## -description


Gets the coordinates of a  footer for a specified item in a list-view control. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774929(v=VS.85).aspx">LVM_GETFOOTERITEMRECT</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param iItem [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the item in the list-view control.


### -param prc [in, out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure to receive the coordinates. The calling application is responsible for allocating this structure. The coordinates received are expressed as client coordinates.

