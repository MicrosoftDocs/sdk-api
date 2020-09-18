---
UID: NF:fdi.FDICreate
title: FDICreate function (fdi.h)
description: The FDICreate function creates an FDI context.
helpviewer_keywords: ["FDICreate","FDICreate function [Windows API]","cpu80286","cpu80386","cpuUNKNOWN","fdi/FDICreate","winprog.fdicreate"]
old-location: winprog\fdicreate.htm
tech.root: winprog
ms.assetid: 90634725-b7a8-4369-8a91-684debee9548
ms.date: 12/05/2018
ms.keywords: FDICreate, FDICreate function [Windows API], cpu80286, cpu80386, cpuUNKNOWN, fdi/FDICreate, winprog.fdicreate
req.header: fdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - FDICreate
 - fdi/FDICreate
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
 - FDICreate
---

# FDICreate function


## -description

The <b>FDICreate</b> function creates an FDI context.

## -parameters

### -param pfnalloc [in]

Pointer to an application-defined callback function to allocate memory. The function should be declared using the <a href="/windows/desktop/api/fdi/nf-fdi-fnalloc">FNALLOC</a> macro.

### -param pfnfree [in]

Pointer to an application-defined callback function to free previously allocated memory. The function should be declared using the <a href="/windows/desktop/api/fdi/nf-fdi-fnfree">FNFREE</a> macro.

### -param pfnopen [in]

Pointer to an application-defined callback function to open a file. The function should be declared using the <a href="/windows/desktop/api/fdi/nf-fdi-fnopen">FNOPEN</a> macro.

### -param pfnread [in]

Pointer to an application-defined callback function to read data from a file. The function should be declared using the <a href="/windows/desktop/api/fdi/nf-fdi-fnread">FNREAD</a> macro.

### -param pfnwrite [in]

Pointer to an application-defined callback function to write data to a file. The function should be declared using the <a href="/windows/desktop/api/fdi/nf-fdi-fnwrite">FNWRITE</a> macro.

### -param pfnclose [in]

Pointer to an application-defined callback function to close a file. The function should be declared using the <a href="/windows/desktop/api/fdi/nf-fdi-fnclose">FNCLOSE</a> macro.

### -param pfnseek [in]

Pointer to an application-defined callback function to move a file pointer to the specified location. The function should be declared using the <a href="/windows/desktop/api/fdi/nf-fdi-fnseek">FNSEEK</a> macro.

### -param cpuType [in]

In the 16-bit version of FDI, specifies the CPU type and can be any of the following values.

<div class="alert"><b>Note</b>  Expressing the <b>cpuUNKNOWN</b> value is recommended.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="cpuUNKNOWN"></a><a id="cpuunknown"></a><a id="CPUUNKNOWN"></a><dl>
<dt><b>cpuUNKNOWN</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
FDI should determine the CPU type.

</td>
</tr>
<tr>
<td width="40%"><a id="cpu80286"></a><a id="CPU80286"></a><dl>
<dt><b>cpu80286</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Only 80286 instructions can be used.

</td>
</tr>
<tr>
<td width="40%"><a id="cpu80386"></a><a id="CPU80386"></a><dl>
<dt><b>cpu80386</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
80386 instructions can be used.

</td>
</tr>
</table>

### -param perf [in, out]

Pointer to an <a href="/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure that receives the error information.

## -returns

If the function succeeds, it returns a non-<b>NULL</b> HFDI context pointer; otherwise, it returns <b>NULL</b>.

Extended error information is provided in the <a href="/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure.

## -see-also

<a href="/windows/desktop/api/fdi/nf-fdi-fdidestroy">FDIDestroy</a>