---
UID: NF:commctrl.Header_GetItemDropDownRect
title: Header_GetItemDropDownRect macro
author: windows-sdk-content
description: Gets the coordinates of the drop-down button for a specified item in a header control. The header control must be of type HDF_SPLITBUTTON. Use this macro or send the HDM_GETITEMDROPDOWNRECT message explicitly.
old-location: controls\Header_GetItemDropDownRect.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getitemdropdownrect.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: Header_GetItemDropDownRect, Header_GetItemDropDownRect macro [Windows Controls], _shell_Header_GetItemDropDownRect, _shell_Header_GetItemDropDownRect_cpp, commctrl/Header_GetItemDropDownRect, controls.Header_GetItemDropDownRect, controls._shell_Header_GetItemDropDownRect
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
 - Header_GetItemDropDownRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Header_GetItemDropDownRect macro


## -description


Gets the coordinates of the drop-down button for a specified item in a header control. The header control must be of type <b>HDF_SPLITBUTTON</b>. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775339(v=VS.85).aspx">HDM_GETITEMDROPDOWNRECT</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the header control.


### -param iItem [in]

Type: <b>int</b>

The zero-based index of the header control item for which to retrieve the bounding rectangle.


### -param lprc [in, out]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure to receive the bounding rectangle information. The message sender is responsible for allocating this structure. The coordinates returned in the <b>RECT</b> structure are expressed as screen coordinates.

