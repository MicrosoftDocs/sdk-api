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

# IX509EnrollmentPolicyServer::Export


## -description


The <b>Export</b> method exports templates and object identifiers associated with the certificate enrollment policy (CEP) server to a buffer.


## -parameters




### -param exportFlags [in]

An <a href="https://msdn.microsoft.com/219f58af-66e8-4a89-8908-89308fc182d8">X509EnrollmentPolicyExportFlags</a> enumeration value that specifies what to export. This can be a bitwise OR of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ExportTemplates"></a><a id="exporttemplates"></a><a id="EXPORTTEMPLATES"></a><dl>
<dt><b>ExportTemplates</b></dt>
</dl>
</td>
<td width="60%">
Export templates.

</td>
</tr>
<tr>
<td width="40%"><a id="ExportOIDs"></a><a id="exportoids"></a><a id="EXPORTOIDS"></a><dl>
<dt><b>ExportOIDs</b></dt>
</dl>
</td>
<td width="60%">
Export custom object identifiers.

</td>
</tr>
</table>
 


### -param pVal [out, retval]

Pointer to a <b>VARIANT</b> of type <b>VT_ARRAY|VT_UI1</b> that receives the templates and object identifiers.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVal</i> parameter must not be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The <i>exportFlags</i> parameter must contain <b>ExportTemplates</b> or <b>ExportOIDs</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a> has not been initialized.

</td>
</tr>
</table>
 




## -remarks



To prevent memory leaks, you must free the <b>VARIANT</b> returned by this function.

You must call <a href="https://msdn.microsoft.com/5b617c6e-91bc-4a22-acd6-41083102850a">LoadPolicy</a> before calling this function and after calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> for the exported data to be meaningful.




## -see-also




<a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a>
 

 

