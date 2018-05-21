---
UID: NE:certenroll.InnerRequestLevel
title: InnerRequestLevel
author: windows-driver-content
description: Specifies the containment level of a certificate request within a PKCS #7 or Certificate Management over CMS (CMC) request.
old-location: security\innerrequestlevel_enum.htm
old-project: SecCertEnroll
ms.assetid: 57b16024-5347-4218-90a7-d85e403aacf0
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: InnerRequestLevel, InnerRequestLevel enumeration [Security], LevelInnermost, LevelNext, certenroll/InnerRequestLevel, certenroll/LevelInnermost, certenroll/LevelNext, security.innerrequestlevel_enum
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: InnerRequestLevel
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CertEnroll.h
api_name:
-	InnerRequestLevel
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# InnerRequestLevel enumeration


## -description


The <b>InnerRequestLevel</b> enumeration type specifies the containment level of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a> within a PKCS #7 or <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Management over CMS</a> (CMC) request. This enumeration is used by the <a href="https://msdn.microsoft.com/5ade7824-d95a-492d-aadf-487422386500">GetInnerRequest</a> method on the <a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a> interface and inherited by the <a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a> and <a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a> interfaces. You can use the enumeration values to retrieve the innermost nested certificate or to iterate through all of the nesting levels.


## -enum-fields




### -field LevelInnermost

Use to retrieve the most deeply nested request.


### -field LevelNext

Use to retrieve the request at the next nesting level.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/5ade7824-d95a-492d-aadf-487422386500">GetInnerRequest</a>
 

 

