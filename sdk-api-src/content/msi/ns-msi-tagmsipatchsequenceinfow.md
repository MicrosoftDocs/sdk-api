---
UID: NS:msi.tagMSIPATCHSEQUENCEINFOW
title: tagMSIPATCHSEQUENCEINFOW
author: windows-sdk-content
description: The MSIPATCHSEQUENCEINFO structure is used by the MsiDeterminePatchSequence and MsiDetermineApplicablePatches functions.
old-location: setup\msipatchsequenceinfo.htm
old-project: msi
ms.assetid: 75f76d85-39f6-4a2c-8b5f-1238639a2014
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PMSIPATCHSEQUENCEINFOW, MSIPATCHSEQUENCEINFO, MSIPATCHSEQUENCEINFO structure, MSIPATCHSEQUENCEINFOA, MSIPATCHSEQUENCEINFOW, MSIPATCH_DATATYPE_PATCHFILE, MSIPATCH_DATATYPE_XMLBLOB, MSIPATCH_DATATYPE_XMLPATH, PMSIPATCHSEQUENCEINFO, PMSIPATCHSEQUENCEINFO structure pointer, msi/MSIPATCHSEQUENCEINFO, msi/MSIPATCHSEQUENCEINFOA, msi/MSIPATCHSEQUENCEINFOW, msi/PMSIPATCHSEQUENCEINFO, setup.msipatchsequenceinfo, tagMSIPATCHSEQUENCEINFOW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: msi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MSIPATCHSEQUENCEINFOW (Unicode) and MSIPATCHSEQUENCEINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MSIPATCHSEQUENCEINFOW, *PMSIPATCHSEQUENCEINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msi.h
api_name:
 - MSIPATCHSEQUENCEINFO
 - MSIPATCHSEQUENCEINFOA
 - MSIPATCHSEQUENCEINFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagMSIPATCHSEQUENCEINFOW structure


## -description


The <b>MSIPATCHSEQUENCEINFO</b> structure  is used by the <a href="https://msdn.microsoft.com/f82e7d42-f0cd-4d25-b56f-7e423cb64cfd">MsiDeterminePatchSequence</a> and <a href="https://msdn.microsoft.com/2362d1dd-695e-48a3-b8ef-4516952ed253">MsiDetermineApplicablePatches</a> functions.


## -struct-fields




### -field szPatchData

Pointer to the path of a patch file, an XML blob, or an XML file.


### -field ePatchDataType

Qualifies <b>szPatchData</b> as a patch file, an XML blob, or an XML file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIPATCH_DATATYPE_PATCHFILE"></a><a id="msipatch_datatype_patchfile"></a><dl>
<dt><b>MSIPATCH_DATATYPE_PATCHFILE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The <b>szPatchData</b> member refers to a path of a patch file.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIPATCH_DATATYPE_XMLPATH"></a><a id="msipatch_datatype_xmlpath"></a><dl>
<dt><b>MSIPATCH_DATATYPE_XMLPATH</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The <b>szPatchData</b> member refers to a path of a XML file.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIPATCH_DATATYPE_XMLBLOB"></a><a id="msipatch_datatype_xmlblob"></a><dl>
<dt><b>MSIPATCH_DATATYPE_XMLBLOB</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The <b>szPatchData</b> member refers to an XML blob.

</td>
</tr>
</table>
 


### -field dwOrder

Set to an integer that indicates the sequence of the patch in the order of application. The sequence starts with 0. If a patch is not applicable to the specified .msi file, or if the function fails, <b>dwOrder</b> is set to -1.


### -field uStatus

Set to ERROR_SUCCESS or the corresponding Win32 error code.


## -see-also




<a href="https://msdn.microsoft.com/2362d1dd-695e-48a3-b8ef-4516952ed253">MsiDetermineApplicablePatches</a>



<a href="https://msdn.microsoft.com/f82e7d42-f0cd-4d25-b56f-7e423cb64cfd">MsiDeterminePatchSequence</a>



<a href="https://msdn.microsoft.com/850b598a-338e-4f84-8336-01e962256a08">Not Supported in Windows Installer 2.0 and earlier</a>
 

 

