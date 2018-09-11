---
UID: NF:wincrypt.CertRDNValueToStrA
title: CertRDNValueToStrA function
author: windows-sdk-content
description: The CertRDNValueToStr function converts a name in a CERT_RDN_VALUE_BLOB to a null-terminated character string.
old-location: security\certrdnvaluetostr.htm
tech.root: seccrypto
ms.assetid: c1e0af19-320e-411e-85bf-c7f01befcac4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CertRDNValueToStr, CertRDNValueToStr function [Security], CertRDNValueToStrA, CertRDNValueToStrW, _crypto2_certrdnvaluetostr, security.certrdnvaluetostr, wincrypt/CertRDNValueToStr, wincrypt/CertRDNValueToStrA, wincrypt/CertRDNValueToStrW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertRDNValueToStrW (Unicode) and CertRDNValueToStrA (ANSI)
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
 - CertRDNValueToStr
 - CertRDNValueToStrA
 - CertRDNValueToStrW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertRDNValueToStrA function


## -description


The <b>CertRDNValueToStr</b> function converts a name in a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_RDN_VALUE_BLOB</a> to a <b>null</b>-terminated character string.


## -parameters




### -param dwValueType [in]

Indicates the kind of RDN value to be converted.

This can be one of the following values:

<ul>
<li>CERT_RDN_ANY_TYPE</li>
<li>CERT_RDN_ENCODED_BLOB</li>
<li>CERT_RDN_OCTET_STRING</li>
<li>CERT_RDN_NUMERIC_STRING</li>
<li>CERT_RDN_PRINTABLE_STRING</li>
<li>CERT_RDN_TELETEX_STRING</li>
<li>CERT_RDN_T61_STRING</li>
<li>CERT_RDN_VIDEOTEX_STRING</li>
<li>CERT_RDN_IA5_STRING</li>
<li>CERT_RDN_GRAPHIC_STRING</li>
<li>CERT_RDN_VISIBLE_STRING</li>
<li>CERT_RDN_ISO646_STRING</li>
<li>CERT_RDN_GENERAL_STRING</li>
<li>CERT_RDN_UNIVERSAL_STRING</li>
<li>CERT_RDN_INT4_STRING</li>
<li>CERT_RDN_BMP_STRING</li>
<li>CERT_RDN_UNICODE_STRING</li>
<li>CERT_RDN_UTF8_STRING</li>
</ul>

### -param pValue [in]

A pointer to an 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_RDN_VALUE_BLOB</a> of a type appropriate for the <i>dwValueType</i>.


### -param psz [out]

A pointer to a buffer to receive the returned string.


### -param csz [in]

Size, in characters, allocated for the returned string. The size must include the terminating <b>NULL</b> character. 



## -returns



Returns the number of characters converted, including the terminating <b>NULL</b> character. If <i>psz</i> is <b>NULL</b> or <i>csz</i> is zero, returns the required size of the destination string.




## -remarks



If <i>psz</i> is not <b>NULL</b> and <i>csz</i> is not zero, the returned <i>psz</i> is always a possibly empty <b>null</b>-terminated string.




## -see-also




<a href="https://msdn.microsoft.com/b3d96de8-5cbc-4ccb-b759-6757520bbda3">CertNameToStr</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Data Conversion Functions</a>
 

 

