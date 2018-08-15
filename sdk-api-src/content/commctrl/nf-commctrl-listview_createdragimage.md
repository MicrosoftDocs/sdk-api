---
UID: NF:commctrl.ListView_CreateDragImage
title: ListView_CreateDragImage macro
author: windows-sdk-content
description: Creates a drag image list for the specified item. You can use this macro or send the LVM_CREATEDRAGIMAGE message explicitly.
old-location: controls\ListView_CreateDragImage.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_createdragimage.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListView_CreateDragImage, ListView_CreateDragImage macro [Windows Controls], _win32_ListView_CreateDragImage, _win32_ListView_CreateDragImage_cpp, commctrl/ListView_CreateDragImage, controls.ListView_CreateDragImage, controls._win32_ListView_CreateDragImage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.redist: 
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
 - ListView_CreateDragImage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_CreateDragImage macro


## -description


Creates a drag image list for the specified item. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774890(v=VS.85).aspx">LVM_CREATEDRAGIMAGE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param i

Type: <b>int</b>

The index of the item. 


### -param lpptUpLeft

Type: <b>LPPOINT</b>

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that receives the initial location of the upper-left corner of the image, in view coordinates. 


## -remarks



Your application is responsible for destroying the image list when it is no longer needed.



