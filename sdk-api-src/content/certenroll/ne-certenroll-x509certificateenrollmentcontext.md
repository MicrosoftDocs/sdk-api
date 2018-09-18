---
UID: NE:certenroll.X509CertificateEnrollmentContext
title: X509CertificateEnrollmentContext
author: windows-sdk-content
description: Specifies the nature of the end entity for which the certificate is intended.
old-location: security\x509certificateenrollmentcontext_enum.htm
tech.root: seccertenroll
ms.assetid: 2db0e129-a566-47ba-ab57-53c7db09e8e3
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, X509CertificateEnrollmentContext, X509CertificateEnrollmentContext enumeration [Security], certenroll/ContextAdministratorForceMachine, certenroll/ContextMachine, certenroll/ContextUser, certenroll/X509CertificateEnrollmentContext, security.x509certificateenrollmentcontext_enum
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
 - X509CertificateEnrollmentContext
product: Windows
targetos: Windows
req.typenames: X509CertificateEnrollmentContext
req.redist: 
---

# X509CertificateEnrollmentContext enumeration


## -description


The <b>X509CertificateEnrollmentContext</b> enumeration  specifies the nature of the end entity for which the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate</a> is intended. This enumeration is used by the following interfaces:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a>
</li>
</ul>



## -enum-fields




### -field ContextNone


### -field ContextUser

The certificate is intended for an end user.


### -field ContextMachine

The certificate is intended for a computer.


### -field ContextAdministratorForceMachine

The certificate is being requested by an administrator acting on the behalf of a computer.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>
 

 

