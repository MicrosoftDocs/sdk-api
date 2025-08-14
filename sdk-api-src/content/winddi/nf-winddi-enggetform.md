---
UID: NF:winddi.EngGetForm
title: EngGetForm function (winddi.h)
description: The EngGetForm function gets the FORM_INFO_1 details for the specified form.
helpviewer_keywords: ["EngGetForm","EngGetForm function [Display Devices]","display.enggetform","gdifncs_178cf402-6353-453e-99c8-0164b0552231.xml","winddi/EngGetForm"]
old-location: display\enggetform.htm
tech.root: display
ms.assetid: b5cc37b1-3e5e-4d3b-b23f-1f737c8dcd28
ms.date: 12/05/2018
ms.keywords: EngGetForm, EngGetForm function [Display Devices], display.enggetform, gdifncs_178cf402-6353-453e-99c8-0164b0552231.xml, winddi/EngGetForm
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngGetForm
 - winddi/EngGetForm
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngGetForm
---

# EngGetForm function


## -description

The <b>EngGetForm</b> function gets the FORM_INFO_1 details for the specified form.

## -parameters

### -param hPrinter [in]

Handle to the printer for which the form is being specified.

### -param pFormName [in]

Pointer to a string that specifies the name of the form.

### -param Level [in]

Specifies the version of the form structure to which <i>pForm</i> points. This value must be 1, which indicates that the form information will be returned in a FORM_INFO_1 structure.

### -param pForm [in, optional]

Pointer to an array of bytes that receives the initialized FORM_INFO_1 structure.

### -param cbBuf [in]

Specifies the size, in bytes, of <i>pForm</i>.

### -param pcbNeeded [out]

Pointer to a value that specifies the number of bytes copied into the buffer pointed to by <i>pForm</i> if the function succeeds. The value is the number of bytes required to perform the copy if <i>cbBuf</i> is too small.

## -returns

<b>EngGetForm</b> returns <b>TRUE</b> if the form structure is successfully copied into <i>pForm</i>. Otherwise, it logs an error message and returns <b>FALSE</b>. To get the error information, call <a href="/windows/desktop/api/winddi/nf-winddi-enggetlasterror">EngGetLastError</a>.

## -remarks

<b>EngGetForm</b> returns a FORM_INFO_1 structure (described in the Microsoft Windows SDK documentation) containing the form data associated with <i>pFormName</i>. The written data and its size are returned to the caller via <i>pForm</i> and <i>pcbNeeded</i>, respectively. If the array pointed to by <i>pForm</i> is not large enough to hold the form data, the requisite array size is instead returned in <i>pcbNeeded</i>.

To get a list of all supported forms, the printer driver should call <a href="/windows/desktop/api/winddi/nf-winddi-engenumforms">EngEnumForms</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engenumforms">EngEnumForms</a>



<a href="/windows/desktop/api/winddi/nf-winddi-enggetlasterror">EngGetLastError</a>