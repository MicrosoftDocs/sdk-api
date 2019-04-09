---
UID: NF:commctrl.ListView_GetInsertMarkRect
title: ListView_GetInsertMarkRect macro (commctrl.h)
author: windows-sdk-content
description: Gets the rectangle that bounds the insertion point. You can use this macro or send the LVM_GETINSERTMARKRECT message explicitly.
old-location: controls\ListView_GetInsertMarkRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getinsertmarkrect.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_GetInsertMarkRect, ListView_GetInsertMarkRect macro [Windows Controls], _win32_ListView_GetInsertMarkRect, _win32_ListView_GetInsertMarkRect_cpp, commctrl/ListView_GetInsertMarkRect, controls.ListView_GetInsertMarkRect, controls._win32_ListView_GetInsertMarkRect
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
 - ListView_GetInsertMarkRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetInsertMarkRect macro


## -description


Gets the rectangle that bounds the insertion point. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774949(v=VS.85).aspx">LVM_GETINSERTMARKRECT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param rc

Type: <b>LPRECT</b>

<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>

## -remarks



To use <b>ListView_GetInsertMarkRect</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



