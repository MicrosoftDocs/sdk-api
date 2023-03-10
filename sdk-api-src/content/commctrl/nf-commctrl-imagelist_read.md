---
UID: NF:commctrl.ImageList_Read
title: ImageList_Read function (commctrl.h)
description: Reads an image list from a stream.
helpviewer_keywords: ["ImageList_Read","ImageList_Read function [Windows Controls]","_win32_ImageList_Read","_win32_ImageList_Read_cpp","commctrl/ImageList_Read","controls.ImageList_Read","controls._win32_ImageList_Read"]
old-location: controls\ImageList_Read.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_read.htm
ms.date: 12/05/2018
ms.keywords: ImageList_Read, ImageList_Read function [Windows Controls], _win32_ImageList_Read, _win32_ImageList_Read_cpp, commctrl/ImageList_Read, controls.ImageList_Read, controls._win32_ImageList_Read
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageList_Read
 - commctrl/ImageList_Read
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_Read
---

# ImageList_Read function


## -description

Reads an image list from a stream.

## -parameters

### -param pstm

Type: <b>LPSTREAM</b>

A pointer to the stream.

## -returns

Type: <b>HIMAGELIST</b>

Returns the handle to the image list if successful, or <b>NULL</b> otherwise.

