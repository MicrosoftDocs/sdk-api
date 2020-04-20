---
UID: NS:commdlg.tagOFN_NT4A
title: OPENFILENAME_NT4A (commdlg.h)
description: The OPENFILENAME_NT4 structure is identical to OPENFILENAME with _WIN32_WINNT set to 0x0400.helpviewer_keywords: ["*LPOPENFILENAME_NT4A","OPENFILENAME_NT4","OPENFILENAME_NT4 structure [Dialog Boxes]","OPENFILENAME_NT4A","OPENFILENAME_NT4W","_win32_OPENFILENAME_NT4_str","_win32_openfilename_nt4_str_cpp","commdlg/OPENFILENAME_NT4","commdlg/OPENFILENAME_NT4A","commdlg/OPENFILENAME_NT4W","dlgbox.openfilename_nt4_str","winui._win32_openfilename_nt4_str"]
old-location: dlgbox\openfilename_nt4_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\openfilename_nt4.htm
ms.date: 12/05/2018
ms.keywords: '*LPOPENFILENAME_NT4A, OPENFILENAME_NT4, OPENFILENAME_NT4 structure [Dialog Boxes], OPENFILENAME_NT4A, OPENFILENAME_NT4W, _win32_OPENFILENAME_NT4_str, _win32_openfilename_nt4_str_cpp, commdlg/OPENFILENAME_NT4, commdlg/OPENFILENAME_NT4A, commdlg/OPENFILENAME_NT4W, dlgbox.openfilename_nt4_str, winui._win32_openfilename_nt4_str'
f1_keywords:
- commdlg/OPENFILENAME_NT4
dev_langs:
- c++
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OPENFILENAME_NT4W (Unicode) and OPENFILENAME_NT4A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Commdlg.h
api_name:
- OPENFILENAME_NT4
- OPENFILENAME_NT4A
- OPENFILENAME_NT4W
targetos: Windows
req.typenames: OPENFILENAME_NT4A, *LPOPENFILENAME_NT4A
req.redist: 
ms.custom: 19H1
---

# OPENFILENAME_NT4A structure


## -description


The <b>OPENFILENAME_NT4</b> structure is identical to <a href="https://docs.microsoft.com/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> with _WIN32_WINNT set to 0x0400. It allows an application to take advantage of other post-Microsoft Windows NT 4.0 features while running on Microsoft Windows NT 4.0. Also, MFC42 applications must use <b>OPENFILENAME_NT4</b> to avoid heap corruption. This is because Microsoft Foundation Classes (MFC) has classes with embedded <b>OPENFILENAME</b> structures, and you must use the same structure size.
<div class="alert"><b>Note</b>  This structure is provided only for compatibility.</div><div> </div>

## -struct-fields

