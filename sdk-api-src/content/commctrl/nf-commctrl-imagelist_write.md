---
UID: NF:commctrl.ImageList_Write
title: ImageList_Write function (commctrl.h)
description: Writes an image list to a stream. (ImageList_Write)
helpviewer_keywords: ["ImageList_Write","ImageList_Write function [Windows Controls]","_win32_ImageList_Write","_win32_ImageList_Write_cpp","commctrl/ImageList_Write","controls.ImageList_Write","controls._win32_ImageList_Write"]
old-location: controls\ImageList_Write.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_write.htm
ms.date: 12/05/2018
ms.keywords: ImageList_Write, ImageList_Write function [Windows Controls], _win32_ImageList_Write, _win32_ImageList_Write_cpp, commctrl/ImageList_Write, controls.ImageList_Write, controls._win32_ImageList_Write
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
 - ImageList_Write
 - commctrl/ImageList_Write
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
 - ImageList_Write
---

# ImageList_Write function


## -description

Writes an image list to a stream.

## -parameters

### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list.

### -param pstm

Type: <b>LPSTREAM</b>

A pointer to the stream.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.
