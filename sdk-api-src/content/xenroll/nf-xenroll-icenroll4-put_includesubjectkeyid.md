---
UID: NF:xenroll.ICEnroll4.put_IncludeSubjectKeyID
title: ICEnroll4::put_IncludeSubjectKeyID
author: windows-sdk-content
description: Determines whether the subject key ID extension is added to the certificate request that is generated.
old-location: security\icenroll4_includesubjectkeyid.htm
old-project: SecCrypto
ms.assetid: 12150ca2-59cc-402e-b25e-cc98b940ecf8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CEnroll object [Security],IncludeSubjectKeyID property, ICEnroll4 interface [Security],IncludeSubjectKeyID property, ICEnroll4.IncludeSubjectKeyID, ICEnroll4.put_IncludeSubjectKeyID, ICEnroll4::IncludeSubjectKeyID, ICEnroll4::get_IncludeSubjectKeyID, ICEnroll4::put_IncludeSubjectKeyID, IncludeSubjectKeyID property [Security], IncludeSubjectKeyID property [Security],CEnroll object, IncludeSubjectKeyID property [Security],ICEnroll4 interface, put_IncludeSubjectKeyID, security.icenroll4_includesubjectkeyid, xenroll/ICEnroll4::IncludeSubjectKeyID, xenroll/ICEnroll4::get_IncludeSubjectKeyID, xenroll/ICEnroll4::put_IncludeSubjectKeyID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xenroll.h
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
tech.root: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.IncludeSubjectKeyID
 - ICEnroll4.get_IncludeSubjectKeyID
 - ICEnroll4.put_IncludeSubjectKeyID
 - CEnroll.IncludeSubjectKeyID
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# ICEnroll4::put_IncludeSubjectKeyID


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>IncludeSubjectKeyID</b> property determines whether the subject key ID extension is added to the certificate request that is  generated. The object identifier (OID) for the subject key ID extension is "2.5.29.14", which is the defined value of the szOID_SUBJECT_KEY_IDENTIFIER constant in  Wincrypt.h. This property was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

