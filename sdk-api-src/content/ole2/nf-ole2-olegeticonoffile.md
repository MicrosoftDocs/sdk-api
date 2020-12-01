---
UID: NF:ole2.OleGetIconOfFile
title: OleGetIconOfFile function (ole2.h)
description: Returns a handle to a metafile containing an icon and string label for the specified file name.
helpviewer_keywords: ["OleGetIconOfFile","OleGetIconOfFile function [COM]","_com_OleGetIconOfFile","com.olegeticonoffile","ole2/OleGetIconOfFile"]
old-location: com\olegeticonoffile.htm
tech.root: com
ms.assetid: 2fa9cd75-4dc6-45a3-aa62-e82bd28289a5
ms.date: 12/05/2018
ms.keywords: OleGetIconOfFile, OleGetIconOfFile function [COM], _com_OleGetIconOfFile, com.olegeticonoffile, ole2/OleGetIconOfFile
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
 - OleGetIconOfFile
 - ole2/OleGetIconOfFile
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
 - OleGetIconOfFile
---

# OleGetIconOfFile function


## -description

Returns a handle to a metafile containing an icon and string label for the specified file name.

## -parameters

### -param lpszPath [in]

A pointer to a file for which the icon and string are to be requested.

### -param fUseFileAsLabel [in]

Indicates whether to use the file name as the icon label.

## -returns

If the function succeeds, the return value is a handle to a metafile that contains and icon and label for the specified file. If there is no CLSID in the registration database for the file, then the function returns the string "Document". If <i>lpszPath</i> is <b>NULL</b>, the function returns <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-olegeticonofclass">OleGetIconOfClass</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olemetafilepictfromiconandlabel">OleMetafilePictFromIconAndLabel</a>