---
UID: NF:mergemod.IMsmMerge.ExtractFiles
title: IMsmMerge::ExtractFiles
author: windows-sdk-content
description: The ExtractFiles method extracts the embedded .cab file from a module and then writes those files to the destination directory. For more information, see the ExtractFiles method of the Merge object.
old-location: setup\imsmmerge_extractfiles.htm
tech.root: MSI
ms.assetid: e5bafd2d-0750-4aa6-87e8-22ef3cfdd5ff
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ExtractFiles, ExtractFiles method, ExtractFiles method,IMsmMerge interface, IMsmMerge interface,ExtractFiles method, IMsmMerge.ExtractFiles, IMsmMerge::ExtractFiles, _msi_extractfiles_function, mergemod/IMsmMerge::ExtractFiles, setup.imsmmerge_extractfiles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
 - IMsmMerge.ExtractFiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmMerge::ExtractFiles


## -description


The 
<b>ExtractFiles</b> method extracts the embedded .cab file from a module and then writes those files to the destination directory. For more information, see  the 
<a href="https://msdn.microsoft.com/846355d6-32f2-4b04-91dc-acd60445fbd9">ExtractFiles</a> method of the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge</a> object.  

<b>IMsmMerge2::ExtractFiles</b>    Mergemod.dll version 2.0 or later.<div> </div><b>IMsmMerge::ExtractFiles</b>      All Mergemod.dll versions.
			




## -parameters




### -param Path [in]

The fully qualified destination directory. A <b>LPCWSTR</b> may be used in place of a <b>BSTR</b>.


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

<b>ExtractFiles</b> always extracts files using short file names for the path. To use long file names for the path, use the 
<a href="https://msdn.microsoft.com/0ba6adc9-a08f-47a6-b8a8-1624bd856511">ExtractFilesEx</a> function.




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

