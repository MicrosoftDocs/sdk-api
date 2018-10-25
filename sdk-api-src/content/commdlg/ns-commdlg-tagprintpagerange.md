---
UID: NS:commdlg.tagPRINTPAGERANGE
title: tagPRINTPAGERANGE
author: windows-sdk-content
description: Represents a range of pages in a print job. A print job can have more than one page range. This information is supplied in the PRINTDLGEX structure when calling the PrintDlgEx function.
old-location: dlgbox\printpagerange_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\printpagerange.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*LPPRINTPAGERANGE, LPPRINTPAGERANGE, LPPRINTPAGERANGE structure pointer [Dialog Boxes], PRINTPAGERANGE, PRINTPAGERANGE structure [Dialog Boxes], _win32_PRINTPAGERANGE_str, _win32_printpagerange_str_cpp, commdlg/LPPRINTPAGERANGE, commdlg/PRINTPAGERANGE, dlgbox.printpagerange_str, tagPRINTPAGERANGE, winui._win32_printpagerange_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commdlg.h
api_name:
 - PRINTPAGERANGE
product: Windows
targetos: Windows
req.typenames: PRINTPAGERANGE
req.redist: 
---

# tagPRINTPAGERANGE structure


## -description


Represents a range of pages in a print job. A print job can have more than one page range. This information is supplied in the <a href="https://msdn.microsoft.com/e843d2fc-d122-4112-bfc9-9bfb26e865da">PRINTDLGEX</a> structure when calling the <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> function.


## -struct-fields




### -field nFromPage

Type: <b>DWORD</b>

The first page of the range. 


### -field nToPage

Type: <b>DWORD</b>

The last page of the range. 


## -see-also




<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>
 

 

