---
UID: NF:xenroll.ICEnroll4.get_IncludeSubjectKeyID
title: ICEnroll4::get_IncludeSubjectKeyID (xenroll.h)
description: Determines whether the subject key ID extension is added to the certificate request that is generated. (Get)
helpviewer_keywords: ["CEnroll object [Security]","IncludeSubjectKeyID property","ICEnroll4 interface [Security]","IncludeSubjectKeyID property","ICEnroll4.IncludeSubjectKeyID","ICEnroll4.get_IncludeSubjectKeyID","ICEnroll4::IncludeSubjectKeyID","ICEnroll4::get_IncludeSubjectKeyID","ICEnroll4::put_IncludeSubjectKeyID","IncludeSubjectKeyID property [Security]","IncludeSubjectKeyID property [Security]","CEnroll object","IncludeSubjectKeyID property [Security]","ICEnroll4 interface","get_IncludeSubjectKeyID","security.icenroll4_includesubjectkeyid","xenroll/ICEnroll4::IncludeSubjectKeyID","xenroll/ICEnroll4::get_IncludeSubjectKeyID","xenroll/ICEnroll4::put_IncludeSubjectKeyID"]
old-location: security\icenroll4_includesubjectkeyid.htm
tech.root: security
ms.assetid: 12150ca2-59cc-402e-b25e-cc98b940ecf8
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],IncludeSubjectKeyID property, ICEnroll4 interface [Security],IncludeSubjectKeyID property, ICEnroll4.IncludeSubjectKeyID, ICEnroll4.get_IncludeSubjectKeyID, ICEnroll4::IncludeSubjectKeyID, ICEnroll4::get_IncludeSubjectKeyID, ICEnroll4::put_IncludeSubjectKeyID, IncludeSubjectKeyID property [Security], IncludeSubjectKeyID property [Security],CEnroll object, IncludeSubjectKeyID property [Security],ICEnroll4 interface, get_IncludeSubjectKeyID, security.icenroll4_includesubjectkeyid, xenroll/ICEnroll4::IncludeSubjectKeyID, xenroll/ICEnroll4::get_IncludeSubjectKeyID, xenroll/ICEnroll4::put_IncludeSubjectKeyID
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
 - ICEnroll4::get_IncludeSubjectKeyID
 - xenroll/ICEnroll4::get_IncludeSubjectKeyID
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
 - ICEnroll4.IncludeSubjectKeyID
 - ICEnroll4.get_IncludeSubjectKeyID
 - ICEnroll4.put_IncludeSubjectKeyID
 - CEnroll.IncludeSubjectKeyID
---

# ICEnroll4::get_IncludeSubjectKeyID


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>IncludeSubjectKeyID</b> property determines whether the subject key ID extension is added to the certificate request that is  generated. The object identifier (OID) for the subject key ID extension is "2.5.29.14", which is the defined value of the szOID_SUBJECT_KEY_IDENTIFIER constant in  Wincrypt.h. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

This property is read/write.

## -parameters

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>
