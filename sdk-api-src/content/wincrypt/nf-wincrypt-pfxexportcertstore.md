---
UID: NF:wincrypt.PFXExportCertStore
title: PFXExportCertStore function
author: windows-sdk-content
description: Exports the certificates and, if available, the associated private keys from the referenced certificate store.
old-location: security\pfxexportcertstore.htm
old-project: seccrypto
ms.assetid: 003602c6-d6c9-4695-9c60-ffaf0aa02266
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EXPORT_PRIVATE_KEYS, PFXExportCertStore, PFXExportCertStore function [Security], REPORT_NOT_ABLE_TO_EXPORT_PRIVATE_KEY, REPORT_NO_PRIVATE_KEY, _crypto2_pfxexportcertstore, security.pfxexportcertstore, wincrypt/PFXExportCertStore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - PFXExportCertStore
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PFXExportCertStore function


## -description


The <b>PFXExportCertStore</b> function exports the certificates and, if available, the associated private keys from the referenced certificate store. This is an old function kept for compatibility with Internet Explorer 4.0 clients. New applications should use the 
<a href="https://msdn.microsoft.com/e8bd54b1-946f-4c65-8a86-96f0dbec07ff">PfxExportCertStoreEx</a> function that provides enhanced private key security.


## -parameters




### -param hStore [in]

Handle of the certificate store containing the certificates to be exported.


### -param pPFX [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure to contain the PFX packet with the exported certificates and keys. If <i>pPFX</i>-&gt;<i>pbData</i> is <b>NULL</b>, the function calculates the number of bytes needed for the encoded BLOB and returns this in <i>pPFX</i>-&gt;<i>cbData</i>. When the function is called with <i>pPFX</i>-&gt;<i>pbData</i> pointing to an allocated buffer of the needed size, the function copies the encoded bytes into the buffer and updates <i>pPFX</i>-&gt;<i>cbData</i> with the encode byte length.


### -param szPassword [in]

String password used to encrypt and verify the PFX packet. When you have finished using the password, clear the password from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -param dwFlags [in]

Flag values can be set to any combination of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EXPORT_PRIVATE_KEYS"></a><a id="export_private_keys"></a><dl>
<dt><b>EXPORT_PRIVATE_KEYS</b></dt>
</dl>
</td>
<td width="60%">
Private keys are exported as well as the certificates.

</td>
</tr>
<tr>
<td width="40%"><a id="REPORT_NO_PRIVATE_KEY"></a><a id="report_no_private_key"></a><dl>
<dt><b>REPORT_NO_PRIVATE_KEY</b></dt>
</dl>
</td>
<td width="60%">
If a certificate is encountered that has no associated private key, the function returns <b>FALSE</b> with the last error set to either CRYPT_E_NOT_FOUND or NTE_NO_KEY.

</td>
</tr>
<tr>
<td width="40%"><a id="REPORT_NOT_ABLE_TO_EXPORT_PRIVATE_KEY"></a><a id="report_not_able_to_export_private_key"></a><dl>
<dt><b>REPORT_NOT_ABLE_TO_EXPORT_PRIVATE_KEY</b></dt>
</dl>
</td>
<td width="60%">
If a certificate is encountered that has a non-exportable private key, the function returns <b>FALSE</b> and the last error set to NTE_BAD_KEY, NTE_BAD_KEY_STATE, or NTE_PERM.

</td>
</tr>
</table>
 


## -returns



Returns <b>TRUE</b> (nonzero) if the function succeeds, and <b>FALSE</b> (zero) if the function fails. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/e8bd54b1-946f-4c65-8a86-96f0dbec07ff">PFXExportCertStoreEx</a>



<a href="https://msdn.microsoft.com/2c83774a-f2df-4d28-9abd-e39aa507ba88">PFXImportCertStore</a>
 

 

