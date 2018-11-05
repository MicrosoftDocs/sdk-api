---
UID: NF:commctrl.ListView_SetColumnOrderArray
title: ListView_SetColumnOrderArray macro
author: windows-sdk-content
description: Sets the left-to-right order of columns in a list-view control. You can use this macro or send the LVM_SETCOLUMNORDERARRAY message explicitly.
old-location: controls\ListView_SetColumnOrderArray.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setcolumnorderarray.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ListView_SetColumnOrderArray, ListView_SetColumnOrderArray macro [Windows Controls], _win32_ListView_SetColumnOrderArray, _win32_ListView_SetColumnOrderArray_cpp, commctrl/ListView_SetColumnOrderArray, controls.ListView_SetColumnOrderArray, controls._win32_ListView_SetColumnOrderArray
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ListView_SetColumnOrderArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetColumnOrderArray macro


## -description


Sets the left-to-right order of columns in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/9b491832-42cc-4262-8f6c-23cbc2c889bf">LVM_SETCOLUMNORDERARRAY</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


### -param iCount

Type: <b>int</b>

The number of columns in the list-view control.


### -param pi

Type: <b>int*</b>

A pointer to an array specifying the order in which columns should be displayed, from left to right. For example, if the contents of the array are {2,0,1}, the control displays column 2, column 0, and column 1, from left to right. 

