---
UID: NF:vfw.GetSaveFileNamePreviewA
title: GetSaveFileNamePreviewA function (vfw.h)
description: The GetSaveFileNamePreview function selects a file by using the Save As dialog box. The dialog box also allows the user to preview the currently specified file. This function augments the capability found in the GetSaveFileName function. (ANSI)
helpviewer_keywords: ["GetSaveFileNamePreviewA", "vfw/GetSaveFileNamePreviewA"]
old-location: multimedia\getsavefilenamepreview.htm
tech.root: Multimedia
ms.assetid: f6dd3127-b3fb-40bc-892c-34bacb47d9a6
ms.date: 12/05/2018
ms.keywords: GetSaveFileNamePreview, GetSaveFileNamePreview function [Windows Multimedia], GetSaveFileNamePreviewA, GetSaveFileNamePreviewW, _win32_GetSaveFileNamePreview, multimedia.getsavefilenamepreview, vfw/GetSaveFileNamePreview, vfw/GetSaveFileNamePreviewA, vfw/GetSaveFileNamePreviewW
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetSaveFileNamePreviewW (Unicode) and GetSaveFileNamePreviewA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetSaveFileNamePreviewA
 - vfw/GetSaveFileNamePreviewA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - GetSaveFileNamePreview
 - GetSaveFileNamePreviewA
 - GetSaveFileNamePreviewW
---

# GetSaveFileNamePreviewA function


## -description

The <b>GetSaveFileNamePreview</b> function selects a file by using the Save As dialog box. The dialog box also allows the user to preview the currently specified file. This function augments the capability found in the <a href="/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea">GetSaveFileName</a> function.

## -parameters

### -param lpofn

Pointer to an <b>OPENFILENAME</b> structure used to initialize the dialog box. On return, the structure contains information about the user's file selection.

## -returns

Returns a handle to the selected file.

## -remarks

> [!NOTE]
> The vfw.h header defines GetSaveFileNamePreview as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
