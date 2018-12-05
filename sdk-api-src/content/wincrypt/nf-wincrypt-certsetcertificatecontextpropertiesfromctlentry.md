---
UID: NF:wincrypt.CertSetCertificateContextPropertiesFromCTLEntry
title: CertSetCertificateContextPropertiesFromCTLEntry function
author: windows-sdk-content
description: Sets the properties on the certificate context by using the attributes in the specified certificate trust list (CTL) entry.
old-location: security\certsetcertificatecontextpropertiesfromctlentry.htm
tech.root: seccrypto
ms.assetid: b53b046a-68d4-4dc5-ab89-1b30ebd1de60
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: CertSetCertificateContextPropertiesFromCTLEntry, CertSetCertificateContextPropertiesFromCTLEntry function [Security], _crypto2_certsetcertificatecontextpropertiesfromctlentry, security.certsetcertificatecontextpropertiesfromctlentry, wincrypt/CertSetCertificateContextPropertiesFromCTLEntry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertSetCertificateContextPropertiesFromCTLEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertSetCertificateContextPropertiesFromCTLEntry function


## -description


The <b>CertSetCertificateContextPropertiesFromCTLEntry</b> function sets the properties on the certificate context by using the attributes in the specified <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) entry.


## -parameters




### -param pCertContext [in]

A pointer to the <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> whose attributes are to be set.


### -param pCtlEntry [in]

A pointer to the <a href="https://msdn.microsoft.com/ebc63847-b641-4205-b15c-7b32c1426c21">CTL_ENTRY</a> structure used to set the attributes on the certificate.


### -param dwFlags [in]

 A <b>DWORD</b>. This parameter can be set to CERT_SET_PROPERTY_IGNORE_PERSIST_ERROR_FLAG to ignore any persisted error flags.


## -returns



If the function succeeds, the function returns nonzero.

  If the function fails, it returns zero.  For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/ebc63847-b641-4205-b15c-7b32c1426c21">CTL_ENTRY</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

