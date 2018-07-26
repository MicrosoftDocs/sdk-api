---
UID: NF:msi.MsiExtractPatchXMLDataA
title: MsiExtractPatchXMLDataA function
author: windows-sdk-content
description: The MsiExtractPatchXMLData function extracts information from a patch that can be used to determine if the patch applies to a target system.
old-location: setup\msiextractpatchxmldata.htm
old-project: Msi
ms.assetid: b0044783-552d-4492-bb1d-337227dd3e16
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: MsiExtractPatchXMLData, MsiExtractPatchXMLData function, MsiExtractPatchXMLDataA, MsiExtractPatchXMLDataW, msi/MsiExtractPatchXMLData, msi/MsiExtractPatchXMLDataA, msi/MsiExtractPatchXMLDataW, setup.msiextractpatchxmldata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer 3.0 or later on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiExtractPatchXMLDataW (Unicode) and MsiExtractPatchXMLDataA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DRM_LICENSE_ACQ_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiExtractPatchXMLData
 - MsiExtractPatchXMLDataA
 - MsiExtractPatchXMLDataW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiExtractPatchXMLDataA function


## -description


The <b>MsiExtractPatchXMLData</b> function extracts information from a patch  that can be used to determine if the patch applies to a target system. The function returns an XML string that can be provided to <a href="https://msdn.microsoft.com/f82e7d42-f0cd-4d25-b56f-7e423cb64cfd">MsiDeterminePatchSequence</a> and <a href="https://msdn.microsoft.com/2362d1dd-695e-48a3-b8ef-4516952ed253">MsiDetermineApplicablePatches</a> instead of the full patch file. The returned information  can be used to determine whether the patch is applicable.


## -parameters




### -param szPatchPath [in]

The  full path to the patch that is being queried. Pass in as a null-terminated string. This parameter cannot be <b>NULL</b>.


### -param dwReserved [in]

A reserved argument that must be 0 (zero).


### -param szXMLData [out, optional]

A pointer to a buffer to hold the XML string that contains the extracted patch information. This buffer should be large enough to contain the received information. If the buffer is too small, the function returns ERROR_MORE_DATA and sets *<i>pcchXMLData</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.



If <i>szXMLData</i> is set to <b>NULL</b> and <i>pcchXMLData</i> is set to a valid pointer,  the function returns ERROR_SUCCESS and sets *<i>pcchXMLData</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.  The function can then be called again to retrieve the value, with <i>szXMLData</i> buffer large enough to contain *<i>pcchXMLData</i> + 1 characters. 


### -param pcchXMLData [in, out, optional]

A pointer to a variable that specifies the number of <b>TCHAR</b> in the <i>szXMLData</i> buffer. When the function returns, this parameter is set to the size of the requested value whether or not the function copies the value into the specified buffer. The size is returned as the number of <b>TCHAR</b> in the requested value, not including the terminating null character.

If this parameter is set to <b>NULL</b>, the function returns ERROR_INVALID_PARAMETER.


## -returns




					The <b>MsiExtractPatchXMLData</b> function can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The function failed in a way that is not identified by any of the return values in this table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The value does not fit in the provided buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The patch file could not be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_PACKAGE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The patch file could not be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
This error can be returned  if MSXML 3.0 is not installed. 

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/85940940-2002-4cb1-8e29-ba2374bf3796">ExtractPatchXMLData</a> method of the <a href="https://msdn.microsoft.com/fefc3e39-073e-4869-86b7-27d20a3b337b">Installer</a> object uses the <b>MsiExtractPatchXMLData</b> function.




## -see-also




<a href="https://msdn.microsoft.com/2362d1dd-695e-48a3-b8ef-4516952ed253">MsiDetermineApplicablePatches </a>



<a href="https://msdn.microsoft.com/f82e7d42-f0cd-4d25-b56f-7e423cb64cfd">MsiDeterminePatchSequence</a>



<a href="https://msdn.microsoft.com/850b598a-338e-4f84-8336-01e962256a08">Not Supported in Windows Installer 2.0 and earlier</a>
 

 

