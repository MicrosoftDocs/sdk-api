---
UID: NF:xenroll.ICEnroll.freeRequestInfo
title: ICEnroll::freeRequestInfo (xenroll.h)
description: Releases session identifiers when they are no longer needed.
helpviewer_keywords: ["CEnroll object [Security]","freeRequestInfo method","ICEnroll interface [Security]","freeRequestInfo method","ICEnroll.freeRequestInfo","ICEnroll2 interface [Security]","freeRequestInfo method","ICEnroll2::freeRequestInfo","ICEnroll3 interface [Security]","freeRequestInfo method","ICEnroll3::freeRequestInfo","ICEnroll4 interface [Security]","freeRequestInfo method","ICEnroll4::freeRequestInfo","ICEnroll::freeRequestInfo","freeRequestInfo","freeRequestInfo method [Security]","freeRequestInfo method [Security]","CEnroll object","freeRequestInfo method [Security]","ICEnroll interface","freeRequestInfo method [Security]","ICEnroll2 interface","freeRequestInfo method [Security]","ICEnroll3 interface","freeRequestInfo method [Security]","ICEnroll4 interface","security.icenroll4_freerequestinfo","xenroll/ICEnroll2::freeRequestInfo","xenroll/ICEnroll3::freeRequestInfo","xenroll/ICEnroll4::freeRequestInfo","xenroll/ICEnroll::freeRequestInfo"]
old-location: security\icenroll4_freerequestinfo.htm
tech.root: security
ms.assetid: 2d3fd4d4-779f-4e28-9b07-4de17262ac5e
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],freeRequestInfo method, ICEnroll interface [Security],freeRequestInfo method, ICEnroll.freeRequestInfo, ICEnroll2 interface [Security],freeRequestInfo method, ICEnroll2::freeRequestInfo, ICEnroll3 interface [Security],freeRequestInfo method, ICEnroll3::freeRequestInfo, ICEnroll4 interface [Security],freeRequestInfo method, ICEnroll4::freeRequestInfo, ICEnroll::freeRequestInfo, freeRequestInfo, freeRequestInfo method [Security], freeRequestInfo method [Security],CEnroll object, freeRequestInfo method [Security],ICEnroll interface, freeRequestInfo method [Security],ICEnroll2 interface, freeRequestInfo method [Security],ICEnroll3 interface, freeRequestInfo method [Security],ICEnroll4 interface, security.icenroll4_freerequestinfo, xenroll/ICEnroll2::freeRequestInfo, xenroll/ICEnroll3::freeRequestInfo, xenroll/ICEnroll4::freeRequestInfo, xenroll/ICEnroll::freeRequestInfo
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
 - ICEnroll::freeRequestInfo
 - xenroll/ICEnroll::freeRequestInfo
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
 - ICEnroll4.freeRequestInfo
 - ICEnroll3.freeRequestInfo
 - ICEnroll2.freeRequestInfo
 - ICEnroll.freeRequestInfo
 - CEnroll.freeRequestInfo
---

# ICEnroll::freeRequestInfo


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>freeRequestInfo</b> method releases session identifiers when they are no longer needed. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

## -parameters

### -param PKCS7OrPKCS10 [in]

Specifies the session identifier that represents the data.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>