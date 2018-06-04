---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagMSIPATCHSEQUENCEINFOA structure


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
 

 

