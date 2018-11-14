---
UID: NF:mergemod.IMsmMerge2.ExtractFilesEx
title: IMsmMerge2::ExtractFilesEx
author: windows-sdk-content
description: The ExtractFilesEx method extracts the embedded .cab file from a module and then writes those files to the destination directory. For more information, see the ExtractFilesEx method of the Merge object.
old-location: setup\imsmmerge2_extractfilesex.htm
tech.root: msi
ms.assetid: 0ba6adc9-a08f-47a6-b8a8-1624bd856511
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ExtractFilesEx, ExtractFilesEx method, ExtractFilesEx method,IMsmMerge2 interface, IMsmMerge2 interface,ExtractFilesEx method, IMsmMerge2.ExtractFilesEx, IMsmMerge2::ExtractFilesEx, _msi_extractfilesex_function, mergemod/IMsmMerge2::ExtractFilesEx, setup.imsmmerge2_extractfilesex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 2.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge2.ExtractFilesEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mergemod.h
: 
- IMsmMerge2.ExtractFilesEx
: 
---

# IMsmMerge2::ExtractFilesEx


## -description


The 
<b>ExtractFilesEx</b> method extracts the embedded .cab file from a module and then writes those files to the destination directory. For more information, see the 
<a href="https://msdn.microsoft.com/8b063052-4f92-466a-9c52-bda26ed13d5c">ExtractFilesEx</a> method of the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge</a> object. 


## -parameters




### -param Path [in]

The fully qualified destination directory. A <b>LPCWSTR</b> may be used in place of a <b>BSTR</b>.


### -param fLongFileNames [in]

Set to specify using long file names for path segments and final file names.


### -param pFilePaths [out]

A pointer to a memory location. This memory location receives a second pointer to a string enumerator containing a list of fully qualified paths for the files that were extracted. The list is empty if no files can be extracted. This argument may be null. No list is provided if <i>pFilePaths</i> is Null.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_MAKE as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
Could not create the output path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPEN_FAILED as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
Could not create the output file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WRITE_FAULT as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
Could not write data to the output file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unable to access embedded .cab file, or create temporary file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No embedded .cab file was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



Any files in the destination directory with the same name are overwritten. The path is created if it does not already exist.




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

