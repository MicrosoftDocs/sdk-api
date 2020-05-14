---
UID: NF:commctrl.ListView_SetBkImage
title: ListView_SetBkImage macro (commctrl.h)
description: Sets the background image in a list-view control. You can use this macro or send the LVM_SETBKIMAGE message explicitly.helpviewer_keywords: ["ListView_SetBkImage","ListView_SetBkImage macro [Windows Controls]","_win32_ListView_SetBkImage","_win32_ListView_SetBkImage_cpp","commctrl/ListView_SetBkImage","controls.ListView_SetBkImage","controls._win32_ListView_SetBkImage"]
old-location: controls\ListView_SetBkImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setbkimage.htm
ms.date: 12/05/2018
ms.keywords: ListView_SetBkImage, ListView_SetBkImage macro [Windows Controls], _win32_ListView_SetBkImage, _win32_ListView_SetBkImage_cpp, commctrl/ListView_SetBkImage, controls.ListView_SetBkImage, controls._win32_ListView_SetBkImage
f1_keywords:
- commctrl/ListView_SetBkImage
dev_langs:
- c++
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
- ListView_SetBkImage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetBkImage macro


## -description


Sets the background image in a list-view control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-setbkimage">LVM_SETBKIMAGE</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param plvbki

Type: <b>LPLVBKIMAGE</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvbkimagea">LVBKIMAGE</a> structure that contains the new background image information. 


## -remarks



Because the list-view control uses OLE COM to manipulate the background images, the calling application must call <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> before using this macro. It is best to call one of these functions when the application is initialized and call either <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> or <a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oleuninitialize">OleUninitialize</a> when the application is terminating. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-listview_getbkimage">ListView_GetBkImage</a>
 

 

