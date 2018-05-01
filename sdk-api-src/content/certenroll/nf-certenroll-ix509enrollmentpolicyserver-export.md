---
UID: NF:certenroll.IX509EnrollmentPolicyServer.Export
title: IX509EnrollmentPolicyServer::Export method
author: windows-driver-content
description: Exports templates and object identifiers associated with the certificate enrollment policy (CEP) server to a buffer.
old-location: security\ix509enrollmentpolicyserver_export.htm
old-project: SecCertEnroll
ms.assetid: b821329b-2ec6-4f47-ba5f-2e1cd7ffb06f
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: Export method [Security], Export method [Security], IX509EnrollmentPolicyServer interface, Export,IX509EnrollmentPolicyServer.Export, ExportOIDs, ExportTemplates, IX509EnrollmentPolicyServer, IX509EnrollmentPolicyServer interface [Security], Export method, IX509EnrollmentPolicyServer::Export, certenroll/IX509EnrollmentPolicyServer::Export, security.ix509enrollmentpolicyserver_export
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certenroll.h
api_name:
-	IX509EnrollmentPolicyServer.Export
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509EnrollmentPolicyServer::Export method


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
 

 

