---
UID: NF:xenroll.IEnroll4.put_IncludeSubjectKeyID
title: IEnroll4::put_IncludeSubjectKeyID (xenroll.h)
description: The IncludeSubjectKeyID property of IEnroll4 determines whether the subject key ID extension is added to the certificate request that is generated. (Put)
helpviewer_keywords: ["IEnroll4 interface [Security]","IncludeSubjectKeyID property","IEnroll4.IncludeSubjectKeyID","IEnroll4.put_IncludeSubjectKeyID","IEnroll4::IncludeSubjectKeyID","IEnroll4::get_IncludeSubjectKeyID","IEnroll4::put_IncludeSubjectKeyID","IncludeSubjectKeyID property [Security]","IncludeSubjectKeyID property [Security]","IEnroll4 interface","put_IncludeSubjectKeyID","security.ienroll4_includesubjectkeyid","xenroll/IEnroll4::IncludeSubjectKeyID","xenroll/IEnroll4::get_IncludeSubjectKeyID","xenroll/IEnroll4::put_IncludeSubjectKeyID"]
old-location: security\ienroll4_includesubjectkeyid.htm
tech.root: security
ms.assetid: 76b85d63-374c-4ce1-97d4-95f42ddcd53f
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],IncludeSubjectKeyID property, IEnroll4.IncludeSubjectKeyID, IEnroll4.put_IncludeSubjectKeyID, IEnroll4::IncludeSubjectKeyID, IEnroll4::get_IncludeSubjectKeyID, IEnroll4::put_IncludeSubjectKeyID, IncludeSubjectKeyID property [Security], IncludeSubjectKeyID property [Security],IEnroll4 interface, put_IncludeSubjectKeyID, security.ienroll4_includesubjectkeyid, xenroll/IEnroll4::IncludeSubjectKeyID, xenroll/IEnroll4::get_IncludeSubjectKeyID, xenroll/IEnroll4::put_IncludeSubjectKeyID
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnroll4::put_IncludeSubjectKeyID
 - xenroll/IEnroll4::put_IncludeSubjectKeyID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll4.IncludeSubjectKeyID
 - IEnroll4.get_IncludeSubjectKeyID
 - IEnroll4.put_IncludeSubjectKeyID
---

# IEnroll4::put_IncludeSubjectKeyID


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>IncludeSubjectKeyID</b> property determines whether the subject key ID extension is added to the certificate request that is  generated. The <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for the subject key ID extension is "2.5.29.14", which is the defined value of the szOID_SUBJECT_KEY_IDENTIFIER constant in  Wincrypt.h. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

This property is read/write.

## -parameters

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>
