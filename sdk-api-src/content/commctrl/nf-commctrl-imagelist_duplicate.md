---
UID: NF:commctrl.ImageList_Duplicate
title: ImageList_Duplicate function
author: windows-sdk-content
description: Creates a duplicate of an existing image list.
old-location: controls\ImageList_Duplicate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_duplicate.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ImageList_Duplicate, ImageList_Duplicate function [Windows Controls], _win32_ImageList_Duplicate, _win32_ImageList_Duplicate_cpp, commctrl/ImageList_Duplicate, controls.ImageList_Duplicate, controls._win32_ImageList_Duplicate
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
req.dll: Comctl32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_Duplicate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ImageList_Duplicate
: 
---

# ImageList_Duplicate function


## -description


Creates a duplicate of an existing image list. 


## -parameters




### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list to be duplicated. All information contained in the original image list for normal images is copied to the new image list. Overlay images are not copied. 


## -returns



Type: <b>HIMAGELIST</b>

Returns the handle to the new duplicate image list if successful, or <b>NULL</b> otherwise. 



