---
UID: NE:certenroll.PFXExportOptions
title: PFXExportOptions
author: windows-sdk-content
description: Specifies how much of a certificate chain is included when creating a Personal Information Exchange (PFX) message.
old-location: security\pfxexportoptions_enum.htm
tech.root: SecCertEnroll
ms.assetid: 72a3ac43-aebf-4801-9e36-23cf338b18ab
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PFXExportChainNoRoot, PFXExportChainWithRoot, PFXExportEEOnly, PFXExportOptions, PFXExportOptions enumeration [Security], certenroll/PFXExportChainNoRoot, certenroll/PFXExportChainWithRoot, certenroll/PFXExportEEOnly, certenroll/PFXExportOptions, security.pfxexportoptions_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - PFXExportOptions
product: Windows
targetos: Windows
req.typenames: PFXExportOptions
req.redist: 
---

# PFXExportOptions enumeration


## -description


The <b>PFXExportOptions</b> enumeration specifies how much of a certificate chain is included when creating a Personal Information Exchange (PFX) message. The PFX message syntax is defined by the PKCS #12 standard. PFX is a transfer syntax for personal identity information, including <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private keys</a> and <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificates</a>. The enumeration is used by the <a href="https://msdn.microsoft.com/en-us/library/Aa377868(v=VS.85).aspx">CreatePFX</a> method on the <a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a> interface.


## -enum-fields




### -field PFXExportEEOnly

Includes only the end entity certificate.


### -field PFXExportChainNoRoot

Includes the certificate chain without the root <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> certificate.


### -field PFXExportChainWithRoot

Includes the entire certificate chain, including the root certification authority certificate.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377868(v=VS.85).aspx">CreatePFX</a>
 

 

