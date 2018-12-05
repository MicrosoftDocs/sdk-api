---
UID: NS:cryptuiapi._CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO
title: "_CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO"
author: windows-sdk-content
description: Contains information that controls the operation of the CryptUIWizExport function when a certificate is the object being exported.
old-location: security\cryptui_wiz_export_certcontext_info.htm
tech.root: seccrypto
ms.assetid: 6be86c4f-0ac7-43c2-81fb-9767279ebeaf
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: "*PCRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO, CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO, CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO structure [Security], CRYPTUI_WIZ_EXPORT_FORMAT_BASE64, CRYPTUI_WIZ_EXPORT_FORMAT_CRL, CRYPTUI_WIZ_EXPORT_FORMAT_CTL, CRYPTUI_WIZ_EXPORT_FORMAT_DER, CRYPTUI_WIZ_EXPORT_FORMAT_PFX, CRYPTUI_WIZ_EXPORT_FORMAT_PKCS7, PCRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO, PCRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO structure pointer [Security], _CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO, cryptuiapi/CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO, cryptuiapi/PCRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO, security.cryptui_wiz_export_certcontext_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: cryptuiapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptuiapi.h
api_name:
 - CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO
product: Windows
targetos: Windows
req.typenames: CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO, *PCRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO
req.redist: 
---

# _CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO structure


## -description


<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO</b> structure contains information that controls the operation of the <a href="https://msdn.microsoft.com/62537d51-c761-4180-b857-58c819ea66aa">CryptUIWizExport</a> function when a certificate is the object being exported.


## -struct-fields




### -field dwSize

The size, in bytes, of this structure.


### -field dwExportFormat

A value that indicates the export format of the certificate.  This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_FORMAT_DER"></a><a id="cryptui_wiz_export_format_der"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_FORMAT_DER</b></dt>
</dl>
</td>
<td width="60%">
Export in <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) format.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_FORMAT_PFX"></a><a id="cryptui_wiz_export_format_pfx"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_FORMAT_PFX</b></dt>
</dl>
</td>
<td width="60%">
Export in Private Information Exchange (PFX) format.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_FORMAT_PKCS7"></a><a id="cryptui_wiz_export_format_pkcs7"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_FORMAT_PKCS7</b></dt>
</dl>
</td>
<td width="60%">
Export in <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">Public Key Cryptography Standard</a> #7 (<a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">PKCS #7</a>) format.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_FORMAT_BASE64"></a><a id="cryptui_wiz_export_format_base64"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_FORMAT_BASE64</b></dt>
</dl>
</td>
<td width="60%">
Export in base 64 format.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_FORMAT_CRL"></a><a id="cryptui_wiz_export_format_crl"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_FORMAT_CRL</b></dt>
</dl>
</td>
<td width="60%">
Export in <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) format.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_FORMAT_CTL"></a><a id="cryptui_wiz_export_format_ctl"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_FORMAT_CTL</b></dt>
</dl>
</td>
<td width="60%">
Export in <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) format.

</td>
</tr>
</table>
 


### -field fExportChain

Indicates whether the certificate chain should be exported in addition to the certificate. Contains nonzero to export the chain or zero to not export the chain.


### -field fExportPrivateKeys

Indicates whether the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> should be exported in addition to the certificate. Contains nonzero to export the private key or zero to not export the private key.


### -field pwszPassword

A pointer to a null-terminated Unicode string that contains the password used to access the private key.  This is required if <b>fExportPrivateKeys</b> is nonzero and is otherwise ignored.


### -field fStrongEncryption

Indicates whether strong encryption should be used in the export process. Contains nonzero to use strong encryption or zero to use weak encryption. This must be nonzero if <b>dwExportFormat</b> is <b>CRYPTUI_WIZ_EXPORT_FORMAT_PFX</b>. If this is nonzero, the PFX <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> produced is not compatible with Internet Explorer 4.0 or earlier versions.

<b>Note</b>  We recommend that you set this to nonzero; otherwise, a substantially weaker encryption algorithm is used in the export process.


## -see-also




<a href="https://msdn.microsoft.com/3c509bb6-d391-4b59-809c-23466c8196ea">CRYPTUI_WIZ_EXPORT_INFO</a>



<a href="https://msdn.microsoft.com/62537d51-c761-4180-b857-58c819ea66aa">CryptUIWizExport</a>
 

 

