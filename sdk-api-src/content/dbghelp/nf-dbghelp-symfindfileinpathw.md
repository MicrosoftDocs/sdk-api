---
UID: NF:dbghelp.SymFindFileInPathW
title: SymFindFileInPathW function
author: windows-sdk-content
description: Locates a symbol file or executable image.
old-location: base\symfindfileinpath.htm
tech.root: debug
ms.assetid: f85d8cd9-958a-490a-b155-3a9abdeda922
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: SSRVOPT_DWORD, SSRVOPT_DWORDPTR, SSRVOPT_GUIDPTR, SymFindFileInPath, SymFindFileInPath function, SymFindFileInPathW, _win32_symfindfileinpath, base.symfindfileinpath, dbghelp/SymFindFileInPath, dbghelp/SymFindFileInPathW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymFindFileInPathW (Unicode) and SymFindFileInPath (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DbgHelp.dll
 - imagehlp.dll
api_name:
 - SymFindFileInPath
 - SymFindFileInPath
 - SymFindFileInPathW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# SymFindFileInPathW function


## -description


Locates a symbol file or executable image.


## -parameters




### -param hprocess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param SearchPath [in, optional]

The search path. This can be multiple paths separated by semicolons. It can include both directories and symbol servers. If this parameter is <b>NULL</b>, the function uses the search path set using the 
<a href="https://msdn.microsoft.com/564ba1f6-65c6-4c45-bdbf-41ef0dd8a39d">SymSetSearchPath</a> or <a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param FileName [in]

The name of the file. You can specify a path; however, only the file name is used.


### -param id [in, optional]

The first of three identifying parameters (see Remarks).


### -param two [in]

The second of three identifying parameters (see Remarks).


### -param three [in]

The third of three identifying parameters (see Remarks).


### -param flags [in]

The format of the <i>id</i> parameter. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SSRVOPT_DWORD"></a><a id="ssrvopt_dword"></a><dl>
<dt><b>SSRVOPT_DWORD</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The <i>id</i> parameter is a <b>DWORD</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SSRVOPT_DWORDPTR"></a><a id="ssrvopt_dwordptr"></a><dl>
<dt><b>SSRVOPT_DWORDPTR</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The <i>id</i> parameter is a pointer to a <b>DWORD</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SSRVOPT_GUIDPTR"></a><a id="ssrvopt_guidptr"></a><dl>
<dt><b>SSRVOPT_GUIDPTR</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The <i>id</i> parameter is a pointer to a <b>GUID</b>.

</td>
</tr>
</table>
 


### -param FoundFile [out]

A pointer to a buffer that receives the fully qualified path to the symbol file. This buffer must be at least MAX_PATH characters.


### -param callback [in, optional]

A <a href="https://msdn.microsoft.com/e579158e-053d-4c81-a2c3-ac3af3d3a201">SymFindFileInPathProc</a> callback function.


### -param context [in, optional]

A user-defined value or <b>NULL</b>. This value is simply passed to the callback function. This parameter is typically used by an application to pass a pointer to a data structure that provides some context for the callback function.


## -returns



If the server locates a valid symbol file, it returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b> and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns a value that indicates why the symbol file was not returned.




## -remarks



The identifying parameters are filled in as follows:

<ul>
<li>
If DbgHelp is looking for a .pdb file, the <i>id</i> parameter specifies the PDB signature as found in the codeview debug directory of the original image. Parameter <i>two</i> specifies the PDB age. Parameter <i>three</i> is unused and set to zero.

</li>
<li>
If DbgHelp is looking for any other type of image, such as an executable file or .dbg file, the <i>id</i> parameter specifies the TimeDateStamp of the original image as found in its PE header. Parameter <i>two</i> specifies the SizeOfImage field, also extracted from the PE header. Parameter <i>three</i> is unused and set to zero.

</li>
</ul>
All of these values can be obtained by calling <a href="https://msdn.microsoft.com/ee5b0821-2746-467e-9d95-90776882ac95">SymSrvGetFileIndexInfo</a>.

When searching a directory, this function does not verify that the symbol identifiers match by default. To ensure the matching symbol files are located, call the <a href="https://msdn.microsoft.com/15d72415-829f-4ba3-af80-1f3762cbebda">SymSetOptions</a> function with SYMOPT_EXACT_SYMBOLS.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/e579158e-053d-4c81-a2c3-ac3af3d3a201">SymFindFileInPathProc</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>



<a href="https://msdn.microsoft.com/564ba1f6-65c6-4c45-bdbf-41ef0dd8a39d">SymSetSearchPath</a>



<a href="https://msdn.microsoft.com/ee5b0821-2746-467e-9d95-90776882ac95">SymSrvGetFileIndexInfo</a>
 

 

