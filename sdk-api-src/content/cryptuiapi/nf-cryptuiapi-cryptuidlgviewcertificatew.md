---
UID: NF:cryptuiapi.CryptUIDlgViewCertificateW
title: CryptUIDlgViewCertificateW function (cryptuiapi.h)
description: Presents a dialog box that displays a specified certificate.
old-location: security\cryptuidlgviewcertificate.htm
tech.root: SecCrypto
ms.assetid: 5107ff22-78c4-4005-80af-ff45781da6c7
ms.date: 12/05/2018
ms.keywords: CryptUIDlgViewCertificate, CryptUIDlgViewCertificate function [Security], CryptUIDlgViewCertificateA, CryptUIDlgViewCertificateW, cryptuiapi/CryptUIDlgViewCertificate, cryptuiapi/CryptUIDlgViewCertificateA, cryptuiapi/CryptUIDlgViewCertificateW, security.cryptuidlgviewcertificate
f1_keywords:
- cryptuiapi/CryptUIDlgViewCertificate
dev_langs:
- c++
req.header: cryptuiapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CryptUIDlgViewCertificateW (Unicode) and CryptUIDlgViewCertificateA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cryptui.lib
req.dll: Cryptui.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Cryptui.dll
- Ext-MS-Win-security-cryptui-l1-1-0.dll
- ext-ms-win-security-cryptui-l1-1-1.dll
- CertCredProviderOneCore.dll
api_name:
- CryptUIDlgViewCertificate
- CryptUIDlgViewCertificateA
- CryptUIDlgViewCertificateW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptUIDlgViewCertificateW function


## -description


The <b>CryptUIDlgViewCertificate</b> function presents a dialog box that displays a specified certificate.


## -parameters




### -param pCertViewInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_viewcertificate_structa">CRYPTUI_VIEWCERTIFICATE_STRUCT</a> structure that contains information about the certificate to view.


### -param pfPropertiesChanged [out]

Indicates whether any certificate properties were modified by the caller.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_viewcertificate_structa">CRYPTUI_VIEWCERTIFICATE_STRUCT</a>
 

 

