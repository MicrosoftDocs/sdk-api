---
UID: NF:commctrl.ListView_GetColumnOrderArray
title: ListView_GetColumnOrderArray macro
author: windows-sdk-content
description: Gets the current left-to-right order of columns in a list-view control. You can use this macro or send the LVM_GETCOLUMNORDERARRAY message explicitly.
old-location: controls\ListView_GetColumnOrderArray.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getcolumnorderarray.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ListView_GetColumnOrderArray, ListView_GetColumnOrderArray macro [Windows Controls], _win32_ListView_GetColumnOrderArray, _win32_ListView_GetColumnOrderArray_cpp, commctrl/ListView_GetColumnOrderArray, controls.ListView_GetColumnOrderArray, controls._win32_ListView_GetColumnOrderArray
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
 - ListView_GetColumnOrderArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetColumnOrderArray macro


## -description


Gets the current left-to-right order of columns in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb774913(v=VS.85).aspx">LVM_GETCOLUMNORDERARRAY</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param iCount

Type: <b>int</b>

The number of columns in the list-view control.


### -param pi

TBD






#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


#### - lpiArray

Type: <b>int*</b>

A pointer to an array of integers that will receive the index values of the columns in the list-view control. The array must be large enough to hold 
					<i>iCount</i> elements. 

