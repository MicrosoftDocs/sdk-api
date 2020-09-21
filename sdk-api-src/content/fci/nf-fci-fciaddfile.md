---
UID: NF:fci.FCIAddFile
title: FCIAddFile function (fci.h)
description: The FCIAddFile adds a file to the cabinet under construction.
helpviewer_keywords: ["FCIAddFile","FCIAddFile function [Windows API]","fci/FCIAddFile","tcompTYPE_MSZIP","tcompTYPE_NONE","winprog.fciaddfile"]
old-location: winprog\fciaddfile.htm
tech.root: winprog
ms.assetid: f99e8718-853b-4d35-98ae-61a8333dbaba
ms.date: 12/05/2018
ms.keywords: FCIAddFile, FCIAddFile function [Windows API], fci/FCIAddFile, tcompTYPE_MSZIP, tcompTYPE_NONE, winprog.fciaddfile
req.header: fci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: Cabinet.lib
req.dll: Cabinet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FCIAddFile
 - fci/FCIAddFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cabinet.dll
api_name:
 - FCIAddFile
---

# FCIAddFile function


## -description

The <b>FCIAddFile</b> adds a file to the cabinet under construction.

## -parameters

### -param hfci [in]

A valid FCI context handle returned by the <a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a> function.

### -param pszSourceFile [in]

The name of the file to add; this value should include path information.

### -param pszFileName [in]

The name under which to store the file in the cabinet.

### -param fExecute [in]

If set <b>TRUE</b>, the file will be executed when extracted.

### -param pfnfcignc [in]

Pointer to an application-defined callback function to obtain specifications on the next cabinet to create. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet">FNFCIGETNEXTCABINET</a> macro.

### -param pfnfcis [in]

Pointer to an application-defined callback function to update the progress information available to the user. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfcistatus">FNFCISTATUS</a> macro.

### -param pfnfcigoi [in]

Pointer to an application-defined callback function to open a file and retrieve the file date, time, and attributes. The function should be declared using the <a href="/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo">FNFCIGETOPENINFO</a> macro.

### -param typeCompress [in]

The compression type to use.

<div class="alert"><b>Note</b>  To indicate LZX compression, use the <a href="/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow">TCOMPfromLZXWindow</a> macro.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tcompTYPE_NONE"></a><a id="tcomptype_none"></a><a id="TCOMPTYPE_NONE"></a><dl>
<dt><b>tcompTYPE_NONE</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
No compression.

</td>
</tr>
<tr>
<td width="40%"><a id="tcompTYPE_MSZIP"></a><a id="tcomptype_mszip"></a><a id="TCOMPTYPE_MSZIP"></a><dl>
<dt><b>tcompTYPE_MSZIP</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Microsoft ZIP compression.

</td>
</tr>
</table>

## -returns

If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure used to create the FCI context.

## -remarks

When set, the _A_EXEC attribute is added to the file entry in the CAB. This mechanism is used in some Microsoft self-extracting executables, and could be used for this purpose in any custom extraction application.

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>