---
UID: NF:vfw.ICSetStatusProc
title: ICSetStatusProc function (vfw.h)
description: The ICSetStatusProc function sends the address of a status callback function to a compressor. The compressor calls this function during lengthy operations.
helpviewer_keywords: ["ICSetStatusProc","ICSetStatusProc function [Windows Multimedia]","_win32_ICSetStatusProc","multimedia.icsetstatusproc","vfw/ICSetStatusProc"]
old-location: multimedia\icsetstatusproc.htm
tech.root: Multimedia
ms.assetid: 1e59a5ae-ac59-45fd-b80a-1908f1bf0d5e
ms.date: 12/05/2018
ms.keywords: ICSetStatusProc, ICSetStatusProc function [Windows Multimedia], _win32_ICSetStatusProc, multimedia.icsetstatusproc, vfw/ICSetStatusProc
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICSetStatusProc
 - vfw/ICSetStatusProc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICSetStatusProc
---

# ICSetStatusProc function


## -description

The <b>ICSetStatusProc</b> function sends the address of a status callback function to a compressor. The compressor calls this function during lengthy operations.

## -parameters

### -param hic

Handle to the compressor.

### -param dwFlags

Applicable flags. Set to zero.

### -param lParam

Constant specified with the status callback address.

### -param fpfnStatus

Pointer to the status callback function. Specify <b>NULL</b> to indicate no status callbacks should be sent.

## -returns

Returns ICERR_OK if successful or <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>