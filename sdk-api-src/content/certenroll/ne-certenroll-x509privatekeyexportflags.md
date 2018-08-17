---
UID: NE:certenroll.X509PrivateKeyExportFlags
title: X509PrivateKeyExportFlags
author: windows-sdk-content
description: Specifies the export policy for a private key.
old-location: security\x509privatekeyexportflags.htm
old-project: seccertenroll
ms.assetid: a50af298-a579-462f-8744-78aa84070360
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: X509PrivateKeyExportFlags, X509PrivateKeyExportFlags enumeration [Security], XCN_NCRYPT_ALLOW_ARCHIVING_FLAG, XCN_NCRYPT_ALLOW_EXPORT_FLAG, XCN_NCRYPT_ALLOW_EXPORT_NONE, XCN_NCRYPT_ALLOW_PLAINTEXT_ARCHIVING_FLAG, XCN_NCRYPT_ALLOW_PLAINTEXT_EXPORT_FLAG, certenroll/X509PrivateKeyExportFlags, certenroll/XCN_NCRYPT_ALLOW_ARCHIVING_FLAG, certenroll/XCN_NCRYPT_ALLOW_EXPORT_FLAG, certenroll/XCN_NCRYPT_ALLOW_EXPORT_NONE, certenroll/XCN_NCRYPT_ALLOW_PLAINTEXT_ARCHIVING_FLAG, certenroll/XCN_NCRYPT_ALLOW_PLAINTEXT_EXPORT_FLAG, security.x509privatekeyexportflags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: X509PrivateKeyExportFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - X509PrivateKeyExportFlags
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# X509PrivateKeyExportFlags enumeration


## -description


The <b>X509PrivateKeyExportFlags</b> enumeration type specifies the export policy for a <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a>. For a Cryptography API: Next Generation (CNG) key, the policy is stored by the key service provider (KSP), and it is the responsibility of the KSP to enforce the policy. When a  legacy <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic service provider</a> (CSP) is specified, the policy is used when creating the key, and it is the responsibility of the CSP to enforce the policy. This enumeration is used when specifying and retrieving the  <a href="https://msdn.microsoft.com/en-us/library/Aa379002(v=VS.85).aspx">ExportPolicy</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> interface.


## -enum-fields




### -field XCN_NCRYPT_ALLOW_EXPORT_NONE

Export is not allowed. This is the default value.


### -field XCN_NCRYPT_ALLOW_EXPORT_FLAG

The private key can be exported.


### -field XCN_NCRYPT_ALLOW_PLAINTEXT_EXPORT_FLAG

The private key can be exported in plaintext form.


### -field XCN_NCRYPT_ALLOW_ARCHIVING_FLAG

The private key can be exported once for archiving.


### -field XCN_NCRYPT_ALLOW_PLAINTEXT_ARCHIVING_FLAG

The private key can be exported once in plaintext form for archiving.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
 

 

