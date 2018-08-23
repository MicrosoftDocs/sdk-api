---
UID: NE:certenroll.InnerRequestLevel
title: InnerRequestLevel
author: windows-sdk-content
description: Specifies the containment level of a certificate request within a PKCS #7 or Certificate Management over CMS (CMC) request.
old-location: security\innerrequestlevel_enum.htm
old-project: seccertenroll
ms.assetid: 57b16024-5347-4218-90a7-d85e403aacf0
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: InnerRequestLevel, InnerRequestLevel enumeration [Security], LevelInnermost, LevelNext, certenroll/InnerRequestLevel, certenroll/LevelInnermost, certenroll/LevelNext, security.innerrequestlevel_enum
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
req.typenames: InnerRequestLevel
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - InnerRequestLevel
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# InnerRequestLevel enumeration


## -description


The <b>InnerRequestLevel</b> enumeration type specifies the containment level of a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a> within a PKCS #7 or <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">Certificate Management over CMS</a> (CMC) request. This enumeration is used by the <a href="https://msdn.microsoft.com/en-us/library/Aa377662(v=VS.85).aspx">GetInnerRequest</a> method on the <a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a> interface and inherited by the <a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a> interfaces. You can use the enumeration values to retrieve the innermost nested certificate or to iterate through all of the nesting levels.


## -enum-fields




### -field LevelInnermost

Use to retrieve the most deeply nested request.


### -field LevelNext

Use to retrieve the request at the next nesting level.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377662(v=VS.85).aspx">GetInnerRequest</a>
 

 

