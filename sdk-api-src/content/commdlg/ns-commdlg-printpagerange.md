---
UID: NS:commdlg.tagPRINTPAGERANGE
title: PRINTPAGERANGE (commdlg.h)
description: Represents a range of pages in a print job. A print job can have more than one page range. This information is supplied in the PRINTDLGEX structure when calling the PrintDlgEx function.
helpviewer_keywords: ["*LPPRINTPAGERANGE","LPPRINTPAGERANGE","LPPRINTPAGERANGE structure pointer [Dialog Boxes]","PRINTPAGERANGE","PRINTPAGERANGE structure [Dialog Boxes]","_win32_PRINTPAGERANGE_str","_win32_printpagerange_str_cpp","commdlg/LPPRINTPAGERANGE","commdlg/PRINTPAGERANGE","dlgbox.printpagerange_str","winui._win32_printpagerange_str"]
old-location: dlgbox\printpagerange_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\printpagerange.htm
ms.date: 12/05/2018
ms.keywords: '*LPPRINTPAGERANGE, LPPRINTPAGERANGE, LPPRINTPAGERANGE structure pointer [Dialog Boxes], PRINTPAGERANGE, PRINTPAGERANGE structure [Dialog Boxes], _win32_PRINTPAGERANGE_str, _win32_printpagerange_str_cpp, commdlg/LPPRINTPAGERANGE, commdlg/PRINTPAGERANGE, dlgbox.printpagerange_str, winui._win32_printpagerange_str'
req.header: commdlg.h
req.include-header: Windows.h
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
req.typenames: PRINTPAGERANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPRINTPAGERANGE
 - commdlg/tagPRINTPAGERANGE
 - PRINTPAGERANGE
 - commdlg/PRINTPAGERANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commdlg.h
api_name:
 - PRINTPAGERANGE
---

# PRINTPAGERANGE structure


## -description

Represents a range of pages in a print job. A print job can have more than one page range. This information is supplied in the <a href="/windows/win32/api/commdlg/ns-commdlg-printdlgexa">PRINTDLGEX</a> structure when calling the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function.

## -struct-fields

### -field nFromPage

Type: <b>DWORD</b>

The first page of the range.

### -field nToPage

Type: <b>DWORD</b>

The last page of the range.

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>