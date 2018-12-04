---
UID: NF:commctrl.ImageList_GetDragImage
title: ImageList_GetDragImage function
author: windows-sdk-content
description: Retrieves the temporary image list that is used for the drag image. The function also retrieves the current drag position and the offset of the drag image relative to the drag position.
old-location: controls\ImageList_GetDragImage.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_getdragimage.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ImageList_GetDragImage, ImageList_GetDragImage function [Windows Controls], _win32_ImageList_GetDragImage, _win32_ImageList_GetDragImage_cpp, commctrl/ImageList_GetDragImage, controls.ImageList_GetDragImage, controls._win32_ImageList_GetDragImage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_GetDragImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageList_GetDragImage function


## -description


Retrieves the temporary image list that is used for the drag image. The function also retrieves the current drag position and the offset of the drag image relative to the drag position. 


## -parameters




### -param ppt

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that receives the current drag position. Can be <b>NULL</b>. 


### -param pptHotspot

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to a <b>POINT</b> structure that receives the offset of the drag image relative to the drag position. Can be <b>NULL</b>. 


## -returns



Type: <b>HIMAGELIST</b>

Returns the handle to the image list if successful, or <b>NULL</b> otherwise. 




## -remarks



The temporary image list is destroyed when the <a href="https://msdn.microsoft.com/54465b0d-6bbe-4c50-8124-cbf3115d0848">ImageList_EndDrag</a> function is called. To begin a drag operation, use the <a href="https://msdn.microsoft.com/5b262b32-5ec2-4f19-8a76-4c318aec7dc7">ImageList_BeginDrag</a> function. 



