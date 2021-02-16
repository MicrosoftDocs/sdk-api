---
UID: NC:imagehlp.PIMAGEHLP_STATUS_ROUTINE
title: PIMAGEHLP_STATUS_ROUTINE (imagehlp.h)
description: An application-defined callback function used with the BindImageEx function. The status routine is called during the process of the image binding.
helpviewer_keywords: ["BindExpandFileHeaders","BindForwarder","BindForwarderNOT","BindImageComplete","BindImageModified","BindImportModule","BindImportModuleFailed","BindImportProcedure","BindImportProcedureFailed","BindMismatchedSymbols","BindNoRoomInImage","BindOutOfMemory","BindRvaToVaFailed","BindSymbolsNotUpdated","PIMAGEHLP_STATUS_ROUTINE","StatusRoutine","StatusRoutine callback","StatusRoutine callback function","_win32_statusroutine","base.statusroutine","imagehlp/StatusRoutine"]
old-location: base\statusroutine.htm
tech.root: Debug
ms.assetid: 38a6ddee-5ef1-416f-99ca-11a50643fc97
ms.date: 12/05/2018
ms.keywords: BindExpandFileHeaders, BindForwarder, BindForwarderNOT, BindImageComplete, BindImageModified, BindImportModule, BindImportModuleFailed, BindImportProcedure, BindImportProcedureFailed, BindMismatchedSymbols, BindNoRoomInImage, BindOutOfMemory, BindRvaToVaFailed, BindSymbolsNotUpdated, PIMAGEHLP_STATUS_ROUTINE, StatusRoutine, StatusRoutine callback, StatusRoutine callback function, _win32_statusroutine, base.statusroutine, imagehlp/StatusRoutine
req.header: imagehlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIMAGEHLP_STATUS_ROUTINE
 - imagehlp/PIMAGEHLP_STATUS_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Imagehlp.h
api_name:
 - StatusRoutine
---

# PIMAGEHLP_STATUS_ROUTINE callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-bindimageex">BindImageEx</a> function. The status routine is called during the process of the image binding.

The <b>PIMAGEHLP_STATUS_ROUTINE</b> type defines a pointer to this callback function. 
<b>StatusRoutine</b> is a placeholder for the application-defined function name.

## -parameters

### -param Reason [in]

The current status of the bind operation. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BindOutOfMemory"></a><a id="bindoutofmemory"></a><a id="BINDOUTOFMEMORY"></a><dl>
<dt><b>BindOutOfMemory</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Out of memory. The <i>Parameter</i> value is the number of bytes in the allocation attempt.

</td>
</tr>
<tr>
<td width="40%"><a id="BindRvaToVaFailed"></a><a id="bindrvatovafailed"></a><a id="BINDRVATOVAFAILED"></a><dl>
<dt><b>BindRvaToVaFailed</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The relative virtual address is invalid for the image. The <i>Parameter</i> value is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="BindNoRoomInImage"></a><a id="bindnoroominimage"></a><a id="BINDNOROOMINIMAGE"></a><dl>
<dt><b>BindNoRoomInImage</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
No room in the image for new format import table. The <i>Parameter</i> value is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="BindImportModuleFailed"></a><a id="bindimportmodulefailed"></a><a id="BINDIMPORTMODULEFAILED"></a><dl>
<dt><b>BindImportModuleFailed</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Module import failed. The <i>Parameter</i> value is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="BindImportProcedureFailed"></a><a id="bindimportprocedurefailed"></a><a id="BINDIMPORTPROCEDUREFAILED"></a><dl>
<dt><b>BindImportProcedureFailed</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Procedure import failed. The <i>Parameter</i> value is the name of the function.

</td>
</tr>
<tr>
<td width="40%"><a id="BindImportModule"></a><a id="bindimportmodule"></a><a id="BINDIMPORTMODULE"></a><dl>
<dt><b>BindImportModule</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Module import is starting. The <i>Parameter</i> value is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="BindImportProcedure"></a><a id="bindimportprocedure"></a><a id="BINDIMPORTPROCEDURE"></a><dl>
<dt><b>BindImportProcedure</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Procedure import is starting. The <i>Parameter</i> value is the name of the function.

</td>
</tr>
<tr>
<td width="40%"><a id="BindForwarder"></a><a id="bindforwarder"></a><a id="BINDFORWARDER"></a><dl>
<dt><b>BindForwarder</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
The <i>Parameter</i> value is the name of the function forwarded.

</td>
</tr>
<tr>
<td width="40%"><a id="BindForwarderNOT"></a><a id="bindforwardernot"></a><a id="BINDFORWARDERNOT"></a><dl>
<dt><b>BindForwarderNOT</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The <i>Parameter</i> value is the name of the function not forwarded.

</td>
</tr>
<tr>
<td width="40%"><a id="BindImageModified"></a><a id="bindimagemodified"></a><a id="BINDIMAGEMODIFIED"></a><dl>
<dt><b>BindImageModified</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Image modified. The <i>Parameter</i> value is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="BindExpandFileHeaders"></a><a id="bindexpandfileheaders"></a><a id="BINDEXPANDFILEHEADERS"></a><dl>
<dt><b>BindExpandFileHeaders</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
File headers expanded. The <i>Parameter</i> value is the number of bytes

</td>
</tr>
<tr>
<td width="40%"><a id="BindImageComplete"></a><a id="bindimagecomplete"></a><a id="BINDIMAGECOMPLETE"></a><dl>
<dt><b>BindImageComplete</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Binding is complete. For more information on the <i>Parameter</i> value, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="BindMismatchedSymbols"></a><a id="bindmismatchedsymbols"></a><a id="BINDMISMATCHEDSYMBOLS"></a><dl>
<dt><b>BindMismatchedSymbols</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
Checksum did not match. The <i>Parameter</i> value is the name of the symbol file.

</td>
</tr>
<tr>
<td width="40%"><a id="BindSymbolsNotUpdated"></a><a id="bindsymbolsnotupdated"></a><a id="BINDSYMBOLSNOTUPDATED"></a><dl>
<dt><b>BindSymbolsNotUpdated</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
Symbol file was not updated. The <i>Parameter</i> value is the name of the symbol file not updated.

</td>
</tr>
</table>

### -param ImageName [in]

The  name of the file to be bound. This value can be a file name, a partial path, or a full path.

### -param DllName [in]

The name of the DLL.

### -param Va [in]

The computed virtual address.

### -param Parameter [in]

Any additional status information. This value depends on the value of the <i>Reason</i> parameter. For more information, see the code fragment in the following Remarks section.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

The following code fragment describes how to use the <i>Va</i> value when the status is BindImageComplete.


```cpp
case BindImageComplete:
    if (fVerbose) {
        fprintf(stderr, "BIND: Details of binding %s\n", ImageName );
        NewImports = (PIMAGE_BOUND_IMPORT_DESCRIPTOR)Va;
        NewImport = NewImports;
        while (NewImport->OffsetModuleName) {
            fprintf( stderr, "    Import from %s [%x]",
                     (LPSTR)NewImports + NewImport->OffsetModuleName,
                     NewImport->TimeDateStamp
                   );
            if (NewImport->NumberOfModuleForwarderRefs != 0) {
                fprintf( stderr, " with %u forwarders", NewImport-> 
                         NumberOfModuleForwarderRefs );
            }
            fprintf( stderr, "\n" );
            NewForwarder = (PIMAGE_BOUND_FORWARDER_REF)(NewImport+1);
            for (i=0; i<NewImport->NumberOfModuleForwarderRefs; i++) 
            {
                fprintf( stderr, "        Forward to %s [%x]\n",
                   (LPSTR)NewImports + NewForwarder->OffsetModuleName,
                   NewForwarder->TimeDateStamp);
                NewForwarder += 1;
            }
            NewImport = (PIMAGE_BOUND_IMPORT_DESCRIPTOR)NewForwarder;
        }
    }
    break;

```

## -see-also

<a href="/windows/desktop/api/imagehlp/nf-imagehlp-bindimageex">BindImageEx</a>



<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>