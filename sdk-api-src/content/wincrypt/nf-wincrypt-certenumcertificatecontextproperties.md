---
UID: NF:wincrypt.CertEnumCertificateContextProperties
title: CertEnumCertificateContextProperties function
author: windows-sdk-content
description: The CertEnumCertificateContextProperties function retrieves the first or next extended property associated with a certificate context.
old-location: security\certenumcertificatecontextproperties.htm
old-project: SecCrypto
ms.assetid: b7304ab2-432b-40c0-8014-7f8874fa36fa
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CertEnumCertificateContextProperties, CertEnumCertificateContextProperties function [Security], _crypto2_certenumcertificatecontextproperties, security.certenumcertificatecontextproperties, wincrypt/CertEnumCertificateContextProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
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
 - CertEnumCertificateContextProperties
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertEnumCertificateContextProperties function


## -description


The <b>CertEnumCertificateContextProperties</b> function retrieves the first or next extended property associated with a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a>. Used in a loop, this function can retrieve in sequence all of the extended properties associated with a <i>certificate context</i>.


## -parameters




### -param pCertContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure of the certificate containing the properties to be enumerated.


### -param dwPropId [in]

Property number of the last property enumerated. To get the first property, <i>dwPropId</i> is zero. To retrieve subsequent properties, <i>dwPropId</i> is set to the property number returned by the last call to the function. To enumerate all the properties, function calls continue until the function returns zero. 




Applications can call 
<a href="https://msdn.microsoft.com/f766db64-3121-4f70-ac83-ce25ee634efa">CertGetCertificateContextProperty</a> with the <i>dwPropId</i> returned by this function to retrieve that property's data.


## -returns



The return value is a <b>DWORD</b> value that identifies a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context's</a> property. The <b>DWORD</b> value returned by one call of the function can be supplied as the <i>dwPropId</i> in a subsequent call to the function. If there are no more properties to be enumerated or if the function fails, zero is returned.




## -remarks



CERT_KEY_PROV_HANDLE_PROP_ID and CERT_KEY_SPEC_PROP_ID properties are stored as members of the CERT_KEY_CONTEXT_PROP_ID property. They are not enumerated individually.


#### Examples

See 
<a href="https://msdn.microsoft.com/4b5361f5-79b1-4b05-a133-1a394da7d6ee">Example C Program: Listing the Certificates in a Store</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/f766db64-3121-4f70-ac83-ce25ee634efa">CertGetCertificateContextProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Extended Property Functions</a>
 

 

