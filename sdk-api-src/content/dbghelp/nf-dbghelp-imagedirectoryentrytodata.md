---
UID: NF:dbghelp.ImageDirectoryEntryToData
title: ImageDirectoryEntryToData function (dbghelp.h)
description: Obtains access to image-specific data.
helpviewer_keywords: ["IMAGE_DIRECTORY_ENTRY_ARCHITECTURE","IMAGE_DIRECTORY_ENTRY_BASERELOC","IMAGE_DIRECTORY_ENTRY_BOUND_IMPORT","IMAGE_DIRECTORY_ENTRY_COM_DESCRIPTOR","IMAGE_DIRECTORY_ENTRY_DEBUG","IMAGE_DIRECTORY_ENTRY_DELAY_IMPORT","IMAGE_DIRECTORY_ENTRY_EXCEPTION","IMAGE_DIRECTORY_ENTRY_EXPORT","IMAGE_DIRECTORY_ENTRY_GLOBALPTR","IMAGE_DIRECTORY_ENTRY_IAT","IMAGE_DIRECTORY_ENTRY_IMPORT","IMAGE_DIRECTORY_ENTRY_LOAD_CONFIG","IMAGE_DIRECTORY_ENTRY_RESOURCE","IMAGE_DIRECTORY_ENTRY_SECURITY","IMAGE_DIRECTORY_ENTRY_TLS","ImageDirectoryEntryToData","ImageDirectoryEntryToData function","_win32_imagedirectoryentrytodata","base.imagedirectoryentrytodata","dbghelp/ImageDirectoryEntryToData"]
old-location: base\imagedirectoryentrytodata.htm
tech.root: Debug
ms.assetid: 9a4ef9e9-543a-4b1b-ba22-2f1ece19f7e6
ms.date: 12/05/2018
ms.keywords: IMAGE_DIRECTORY_ENTRY_ARCHITECTURE, IMAGE_DIRECTORY_ENTRY_BASERELOC, IMAGE_DIRECTORY_ENTRY_BOUND_IMPORT, IMAGE_DIRECTORY_ENTRY_COM_DESCRIPTOR, IMAGE_DIRECTORY_ENTRY_DEBUG, IMAGE_DIRECTORY_ENTRY_DELAY_IMPORT, IMAGE_DIRECTORY_ENTRY_EXCEPTION, IMAGE_DIRECTORY_ENTRY_EXPORT, IMAGE_DIRECTORY_ENTRY_GLOBALPTR, IMAGE_DIRECTORY_ENTRY_IAT, IMAGE_DIRECTORY_ENTRY_IMPORT, IMAGE_DIRECTORY_ENTRY_LOAD_CONFIG, IMAGE_DIRECTORY_ENTRY_RESOURCE, IMAGE_DIRECTORY_ENTRY_SECURITY, IMAGE_DIRECTORY_ENTRY_TLS, ImageDirectoryEntryToData, ImageDirectoryEntryToData function, _win32_imagedirectoryentrytodata, base.imagedirectoryentrytodata, dbghelp/ImageDirectoryEntryToData
req.header: dbghelp.h
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
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - ImageDirectoryEntryToData
 - dbghelp/ImageDirectoryEntryToData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
 - imagehlp.dll
api_name:
 - ImageDirectoryEntryToData
---

# ImageDirectoryEntryToData function


## -description

Obtains access to image-specific data.

This function has been superseded by the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagedirectoryentrytodataex">ImageDirectoryEntryToDataEx</a> function. Use 
<b>ImageDirectoryEntryToDataEx</b> to retrieve the section header.

## -parameters

### -param Base [in]

The base address of the image.

### -param MappedAsImage [in]

If this parameter is <b>TRUE</b>, the file is mapped by the system as an image. If the flag is <b>FALSE</b>, the file is mapped as a data file by the 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a> function.

### -param DirectoryEntry [in]

The index number of the desired directory entry. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_ARCHITECTURE"></a><a id="image_directory_entry_architecture"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_ARCHITECTURE</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Architecture-specific data

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_BASERELOC"></a><a id="image_directory_entry_basereloc"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_BASERELOC</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Base relocation table

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_BOUND_IMPORT"></a><a id="image_directory_entry_bound_import"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_BOUND_IMPORT</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Bound import directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_COM_DESCRIPTOR"></a><a id="image_directory_entry_com_descriptor"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_COM_DESCRIPTOR</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
COM descriptor table

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_DEBUG"></a><a id="image_directory_entry_debug"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_DEBUG</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Debug directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_DELAY_IMPORT"></a><a id="image_directory_entry_delay_import"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_DELAY_IMPORT</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
Delay import table

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_EXCEPTION"></a><a id="image_directory_entry_exception"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_EXCEPTION</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Exception directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_EXPORT"></a><a id="image_directory_entry_export"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_EXPORT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Export directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_GLOBALPTR"></a><a id="image_directory_entry_globalptr"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_GLOBALPTR</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The relative virtual address of global pointer

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_IAT"></a><a id="image_directory_entry_iat"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_IAT</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
Import address table

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_IMPORT"></a><a id="image_directory_entry_import"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_IMPORT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Import directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_LOAD_CONFIG"></a><a id="image_directory_entry_load_config"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_LOAD_CONFIG</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Load configuration directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_RESOURCE"></a><a id="image_directory_entry_resource"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_RESOURCE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Resource directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_SECURITY"></a><a id="image_directory_entry_security"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_SECURITY</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Security directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_TLS"></a><a id="image_directory_entry_tls"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_TLS</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Thread local storage directory

</td>
</tr>
</table>

### -param Size [out]

A pointer to a variable that receives the size of the data for the directory entry, in bytes.

## -returns

If the function succeeds, the return value is a pointer to the directory entry's data.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>ImageDirectoryEntryToData</b> function is used to obtain access to image-specific data.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagedirectoryentrytodataex">ImageDirectoryEntryToDataEx</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>