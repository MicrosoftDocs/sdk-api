---
UID: NF:certenroll.IX509CertificateTemplateWritable.Commit
title: IX509CertificateTemplateWritable::Commit method
author: windows-driver-content
description: Deletes a template from or saves it to Active Directory.
old-location: security\ix509certificatetemplatewritable_commit.htm
old-project: SecCertEnroll
ms.assetid: ee7d5640-8d06-4a1a-bce2-f76ee6276207
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: Commit method [Security], Commit method [Security], IX509CertificateTemplateWritable interface, Commit,IX509CertificateTemplateWritable.Commit, CommitFlagDeleteTemplate, CommitFlagSaveTemplateGenerateOID, CommitFlagSaveTemplateOverwrite, CommitFlagSaveTemplateUseCurrentOID, IX509CertificateTemplateWritable, IX509CertificateTemplateWritable interface [Security], Commit method, IX509CertificateTemplateWritable::Commit, certenroll/IX509CertificateTemplateWritable::Commit, security.ix509certificatetemplatewritable_commit
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
-	IX509CertificateTemplateWritable.Commit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509CertificateTemplateWritable::Commit method


## -description


The <b>Commit</b> method deletes a template from or saves it to Active Directory.


## -parameters




### -param commitFlags [in]

A <a href="https://msdn.microsoft.com/e228928a-ef11-4caa-b33f-fe25a3a6ff86">CommitTemplateFlags</a> enumeration value that specifies how to save or delete the template. This must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CommitFlagSaveTemplateGenerateOID"></a><a id="commitflagsavetemplategenerateoid"></a><a id="COMMITFLAGSAVETEMPLATEGENERATEOID"></a><dl>
<dt><b>CommitFlagSaveTemplateGenerateOID</b></dt>
</dl>
</td>
<td width="60%">
Save the template and create an object identifier for it.

</td>
</tr>
<tr>
<td width="40%"><a id="CommitFlagSaveTemplateUseCurrentOID"></a><a id="commitflagsavetemplateusecurrentoid"></a><a id="COMMITFLAGSAVETEMPLATEUSECURRENTOID"></a><dl>
<dt><b>CommitFlagSaveTemplateUseCurrentOID</b></dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CommitFlagSaveTemplateOverwrite"></a><a id="commitflagsavetemplateoverwrite"></a><a id="COMMITFLAGSAVETEMPLATEOVERWRITE"></a><dl>
<dt><b>CommitFlagSaveTemplateOverwrite</b></dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CommitFlagDeleteTemplate"></a><a id="commitflagdeletetemplate"></a><a id="COMMITFLAGDELETETEMPLATE"></a><dl>
<dt><b>CommitFlagDeleteTemplate</b></dt>
</dl>
</td>
<td width="60%">
Delete the template.

</td>
</tr>
</table>
 


### -param strServerContext [in]

A <b>BSTR</b> variable that contains the DNS name of the Active Directory server to which the changes will be applied. If this value is <b>NULL</b>, the changes will be applied to the default domain controller.


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
<dt><b>CRYPT_E_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
<b>CommitFlagSaveTemplateGenerateOID</b> was specified in the <i>commitFlags</i> argument but a template with a matching common name or a matching object identifier (OID) already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
<i>CommitFlagDelete</i> was specified in the <i>commitFlags</i> argument and a template with the same Common Name was found but the OID did not match.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDEINED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the appropriate permission to save or delete a template. The caller must have write and delete permission on the template container and template objects in Active Directory. If the caller has delete permission on the template container and objects but does not have delete permission on the OID container and objects, the template will be deleted but the OID will not be.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Either <b>CommitFlagSaveTemplateUseCurrentOID</b> or <b>CommitFlagSaveTemplateOverwrite</b> was specified in the <i>commitFlags</i> argument. These values are not currently used.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
<i>CommitFlagDelete</i> was specified in the <i>commitFlags</i> argument but a template having a matching Common Name (CN) could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a> method is not supported for default templates.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/87660b16-06a8-4a71-8669-24521f1399e4">IX509CertificateTemplateWritable</a> object has not been initialized.

</td>
</tr>
</table>
 




## -remarks



When <b>CommitFlagSaveTemplateGenerateOID</b> is specified in the <i>commitFlags</i> argument, this method will not succeed unless the template and OID containers have already been created. These containers can be created in any of the following ways:

<ul>
<li>Installing an enterprise certification authority on the server.</li>
<li>Launching the Certtmpl.msc snap-in.</li>
<li>Using the <b>Certutil.exe -installDefaultTemplates</b> command to install the default templates.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/87660b16-06a8-4a71-8669-24521f1399e4">IX509CertificateTemplateWritable</a>
 

 

