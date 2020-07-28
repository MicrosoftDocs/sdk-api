---
UID: NF:commctrl.Header_GetOrderArray
title: Header_GetOrderArray macro (commctrl.h)
description: Gets the current left-to-right order of items in a header control. You can use this macro or send the HDM_GETORDERARRAY message explicitly.
helpviewer_keywords: ["Header_GetOrderArray","Header_GetOrderArray macro [Windows Controls]","_win32_Header_GetOrderArray","_win32_Header_GetOrderArray_cpp","commctrl/Header_GetOrderArray","controls.Header_GetOrderArray","controls._win32_Header_GetOrderArray"]
old-location: controls\Header_GetOrderArray.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getorderarray.htm
ms.date: 12/05/2018
ms.keywords: Header_GetOrderArray, Header_GetOrderArray macro [Windows Controls], _win32_Header_GetOrderArray, _win32_Header_GetOrderArray_cpp, commctrl/Header_GetOrderArray, controls.Header_GetOrderArray, controls._win32_Header_GetOrderArray
f1_keywords:
- commctrl/Header_GetOrderArray
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
- Header_GetOrderArray
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Header_GetOrderArray macro


## -description


Gets the current left-to-right order of items in a header control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/hdm-getorderarray">HDM_GETORDERARRAY</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a header control. 


### -param iCount

Type: <b>int</b>

The number of integer elements that 
					<i>lpiArray</i> can hold. This value must be equal to the number of items in the control (see <a href="https://docs.microsoft.com/windows/desktop/Controls/hdm-getitemcount">HDM_GETITEMCOUNT</a>).


### -param lpi

Type: <b>int*</b>

A pointer to an array of integers that receive the index values for items in the header.


## -remarks



The number of elements in <i>lpiArray</i> is specified in <i>iSize</i> and must be equal to the number of items in the control. For example, the following code fragment will reserve enough memory to hold the index values. 


```

int iItems,

    *lpiArray;



// Get memory for buffer

if((iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```




