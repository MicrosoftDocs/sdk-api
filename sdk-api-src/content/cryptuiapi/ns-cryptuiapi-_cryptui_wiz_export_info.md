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

# _CRYPTUI_WIZ_EXPORT_INFO structure


## -description


<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_EXPORT_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_EXPORT_INFO</b> structure contains information that controls the operation of the <a href="https://msdn.microsoft.com/62537d51-c761-4180-b857-58c819ea66aa">CryptUIWizExport</a> function.


## -struct-fields




### -field dwSize

The size, in bytes, of this structure.


### -field pwszExportFileName

A pointer to a null-terminated Unicode string that contains the fully qualified file name to export to. If this member is
not <b>NULL</b> and the <b>CRYPTUI_WIZ_NO_UI</b> flag in the <i>dwFlags</i> parameter of the <a href="https://msdn.microsoft.com/62537d51-c761-4180-b857-58c819ea66aa">CryptUIWizExport</a> function is not set, this string is
displayed to the user as the default file name. This member is required if the <b>CRYPTUI_WIZ_NO_UI</b> flag is set.  This member is otherwise optional.


### -field dwSubjectChoice

Indicates the type of the subject to export.  This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_CERT_CONTEXT"></a><a id="cryptui_wiz_export_cert_context"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_CERT_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Export the certificate context that is specified in the <b>pCertContext</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_CTL_CONTEXT"></a><a id="cryptui_wiz_export_ctl_context"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_CTL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Export the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) context that is specified in the <b>pCTLContext</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_CRL_CONTEXT"></a><a id="cryptui_wiz_export_crl_context"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_CRL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Export the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) context that is specified in the <b>pCRLContext</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_CERT_STORE"></a><a id="cryptui_wiz_export_cert_store"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_CERT_STORE</b></dt>
</dl>
</td>
<td width="60%">
Export the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> that is specified in the <b>hCertStore</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_CERT_STORE_CERTIFICATES_ONLY"></a><a id="cryptui_wiz_export_cert_store_certificates_only"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_CERT_STORE_CERTIFICATES_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Export only the <a href="https://msdn.microsoft.com/library/windows/hardware/mt484158">certificates</a> from the certificate store that is specified in the <b>hCertStore</b> member.

</td>
</tr>
</table>
 


### -field pCertContext

A pointer to the <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that contains the certificate to export. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_EXPORT_CERT_CONTEXT</b>.


### -field pCTLContext

A pointer to the <a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure that contains the CTL to export. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_EXPORT_CTL_CONTEXT</b>.


### -field pCRLContext

A pointer to the <a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a> structure that contains the CRL to export. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_EXPORT_CRL_CONTEXT</b>.


### -field hCertStore

A handle to the certificate store to export. This member is used if the <b>dwSubjectChoice</b> member contains <b>CRYPTUI_WIZ_EXPORT_CERT_STORE</b> or <b>CRYPTUI_WIZ_EXPORT_CERT_STORE_CERTIFICATES_ONLY</b>.


### -field cStores

The number of elements in the <b>rghStores</b> array.


### -field rghStores

An array of extra certificate stores to search for certificates in the trust chain if the chain is being exported with a certificate.
This member is ignored if <b>dwSubjectChoice</b> is anything other than the   <b>CRYPTUI_WIZ_EXPORT_CERT_CONTEXT</b> value. The <b>cStores</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/62537d51-c761-4180-b857-58c819ea66aa">CryptUIWizExport</a>
 

 

