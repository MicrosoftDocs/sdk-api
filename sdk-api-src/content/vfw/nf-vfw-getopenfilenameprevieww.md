---
UID: NF:vfw.GetOpenFileNamePreviewW
title: GetOpenFileNamePreviewW function (vfw.h)
description: The GetOpenFileNamePreview function selects a file by using the Open dialog box. The dialog box also allows the user to preview the currently specified AVI file. This function augments the capability found in the GetOpenFileName function.helpviewer_keywords: ["GetOpenFileNamePreview","GetOpenFileNamePreview function [Windows Multimedia]","GetOpenFileNamePreviewA","GetOpenFileNamePreviewW","_win32_GetOpenFileNamePreview","multimedia.getopenfilenamepreview","vfw/GetOpenFileNamePreview","vfw/GetOpenFileNamePreviewA","vfw/GetOpenFileNamePreviewW"]
old-location: multimedia\getopenfilenamepreview.htm
tech.root: Multimedia
ms.assetid: f0247d7b-47e2-436b-a783-ae78974f8340
ms.date: 12/05/2018
ms.keywords: GetOpenFileNamePreview, GetOpenFileNamePreview function [Windows Multimedia], GetOpenFileNamePreviewA, GetOpenFileNamePreviewW, _win32_GetOpenFileNamePreview, multimedia.getopenfilenamepreview, vfw/GetOpenFileNamePreview, vfw/GetOpenFileNamePreviewA, vfw/GetOpenFileNamePreviewW
f1_keywords:
- vfw/GetOpenFileNamePreview
dev_langs:
- c++
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetOpenFileNamePreviewW (Unicode) and GetOpenFileNamePreviewA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Msvfw32.dll
api_name:
- GetOpenFileNamePreview
- GetOpenFileNamePreviewA
- GetOpenFileNamePreviewW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetOpenFileNamePreviewW function


## -description



The <b>GetOpenFileNamePreview</b> function selects a file by using the Open dialog box. The dialog box also allows the user to preview the currently specified AVI file. This function augments the capability found in the <a href="https://msdn.microsoft.com/library/ms646927.aspx">GetOpenFileName</a> function.




## -parameters




### -param lpofn

Pointer to an <b>OPENFILENAME</b> structure used to initialize the dialog box. On return, the structure contains information about the user's file selection.


## -returns



Returns a handle to the selected file.



