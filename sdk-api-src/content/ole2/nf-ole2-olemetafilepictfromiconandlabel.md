---
UID: NF:ole2.OleMetafilePictFromIconAndLabel
title: OleMetafilePictFromIconAndLabel function (ole2.h)
description: Creates a metafile in which the specified icon and label are drawn.
helpviewer_keywords: ["OleMetafilePictFromIconAndLabel","OleMetafilePictFromIconAndLabel function [COM]","_ole_OleMetafilePictFromIconAndLabel","com.olemetafilepictfromiconandlabel","ole2/OleMetafilePictFromIconAndLabel"]
old-location: com\olemetafilepictfromiconandlabel.htm
tech.root: com
ms.assetid: 627a79eb-46dd-4df7-a0d6-cab37b73387a
ms.date: 12/05/2018
ms.keywords: OleMetafilePictFromIconAndLabel, OleMetafilePictFromIconAndLabel function [COM], _ole_OleMetafilePictFromIconAndLabel, com.olemetafilepictfromiconandlabel, ole2/OleMetafilePictFromIconAndLabel
req.header: ole2.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleMetafilePictFromIconAndLabel
 - ole2/OleMetafilePictFromIconAndLabel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleMetafilePictFromIconAndLabel
---

# OleMetafilePictFromIconAndLabel function


## -description

Creates a metafile in which the specified icon and label are drawn.

## -parameters

### -param hIcon [in]

Handle to the icon that is to be drawn into the metafile. This parameter can be <b>NULL</b>. If <i>hIcon</i> is <b>NULL</b>, this function returns <b>NULL</b> without creating a metafile.

### -param lpszLabel [in]

The icon label. This parameter can be <b>NULL</b>. If <i>lpszLabel</i> is <b>NULL</b>, the resulting metafile will not include a label.

### -param lpszSourceFile [in]

The path and file name of the icon file. This string can be obtained through the user interface or from the registration database. This parameter can be <b>NULL</b>.

### -param iIconIndex [in]

The location of the icon within the file named by <i>lpszSourceFile</i>, expressed as an offset in bytes from the beginning of file.

## -returns

A global handle to a <a href="/windows/desktop/api/wingdi/ns-wingdi-metafilepict">METAFILEPICT</a> structure containing the icon and label. The metafile uses the MM_ANISOTROPIC mapping mode.

If an error occurs, the returned handle is <b>NULL</b>. In this case, the caller can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to obtain further information.

## -remarks

This function is called by <a href="/windows/desktop/api/ole2/nf-ole2-olegeticonoffile">OleGetIconOfFile</a> and <a href="/windows/desktop/api/ole2/nf-ole2-olegeticonofclass">OleGetIconOfClass</a>.

If <i>lpszSourceFile</i> is not <b>NULL</b> and <i>iIconIndex</i> is not 0, the name of the source file passed in <i>lpszSourceFile</i> and the index passed by <i>iIconIndex</i> are added to the created metafile as a comment record.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-olegeticonofclass">OleGetIconOfClass</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olegeticonoffile">OleGetIconOfFile</a>