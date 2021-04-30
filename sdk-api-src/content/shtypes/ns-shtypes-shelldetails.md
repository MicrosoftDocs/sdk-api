---
UID: NS:shtypes._SHELLDETAILS
title: SHELLDETAILS (shtypes.h)
description: Reports detailed information on an item in a Shell folder.
helpviewer_keywords: ["*LPSHELLDETAILS","LPSHELLDETAILS","LPSHELLDETAILS structure pointer [Windows Shell]","LVCFMT_CENTER","LVCFMT_COL_HAS_IMAGES","LVCFMT_LEFT","LVCFMT_RIGHT","SHELLDETAILS","SHELLDETAILS structure [Windows Shell]","The alignment of the leftmost column is always left-justified and cannot be changed.","_win32_SHELLDETAILS_str","shell.SHELLDETAILS_str","shtypes/LPSHELLDETAILS","shtypes/SHELLDETAILS"]
old-location: shell\SHELLDETAILS_str.htm
tech.root: shell
ms.assetid: 2910debb-b769-4498-bd99-9fbf16567e15
ms.date: 12/05/2018
ms.keywords: '*LPSHELLDETAILS, LPSHELLDETAILS, LPSHELLDETAILS structure pointer [Windows Shell], LVCFMT_CENTER, LVCFMT_COL_HAS_IMAGES, LVCFMT_LEFT, LVCFMT_RIGHT, SHELLDETAILS, SHELLDETAILS structure [Windows Shell], The alignment of the leftmost column is always left-justified and cannot be changed., _win32_SHELLDETAILS_str, shell.SHELLDETAILS_str, shtypes/LPSHELLDETAILS, shtypes/SHELLDETAILS'
req.header: shtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHELLDETAILS, *LPSHELLDETAILS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHELLDETAILS
 - shtypes/_SHELLDETAILS
 - LPSHELLDETAILS
 - shtypes/LPSHELLDETAILS
 - SHELLDETAILS
 - shtypes/SHELLDETAILS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shtypes.h
api_name:
 - SHELLDETAILS
---

# SHELLDETAILS structure


## -description

Reports detailed information on an item in a Shell folder.

## -struct-fields

### -field fmt

Type: <b>int</b>

The alignment of the column heading and the subitem text in the column. This member can be one of the following values.



#### LVCFMT_CENTER

Text is centered.



#### LVCFMT_COL_HAS_IMAGES


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 4.70</a>. Header item contains an image in the image list.



#### LVCFMT_LEFT

Text is left-aligned.



#### LVCFMT_RIGHT

Text is right-aligned.



#####

### -field cxChar

Type: <b>int</b>

The number of average-sized characters in the header.

### -field str

Type: <b><a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a></b>

An <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure that includes a string with the requested information. To convert this structure to a string, use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-strrettobufa">StrRetToBuf</a> or <a href="/windows/desktop/api/shlwapi/nf-shlwapi-strrettostra">StrRetToStr</a>.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof">IShellDetails::GetDetailsOf</a>