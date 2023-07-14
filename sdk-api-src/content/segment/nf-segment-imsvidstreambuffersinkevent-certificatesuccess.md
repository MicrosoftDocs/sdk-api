---
UID: NF:segment.IMSVidStreamBufferSinkEvent.CertificateSuccess
title: IMSVidStreamBufferSinkEvent::CertificateSuccess (segment.h)
description: This topic applies to Windows XP Service Pack 1 or later.
helpviewer_keywords: ["CertificateSuccess","CertificateSuccess method [Microsoft TV Technologies]","CertificateSuccess method [Microsoft TV Technologies]","IMSVidStreamBufferSinkEvent interface","IMSVidStreamBufferSinkEvent interface [Microsoft TV Technologies]","CertificateSuccess method","IMSVidStreamBufferSinkEvent.CertificateSuccess","IMSVidStreamBufferSinkEvent::CertificateSuccess","IMSVidStreamBufferSinkEventCertificateSuccess","mstv.imsvidstreambuffersinkevent_certificatesuccess","segment/IMSVidStreamBufferSinkEvent::CertificateSuccess"]
old-location: mstv\imsvidstreambuffersinkevent_certificatesuccess.htm
tech.root: mstv
ms.assetid: 23ac75ee-02ee-4159-b503-65604a6601cb
ms.date: 12/05/2018
ms.keywords: CertificateSuccess, CertificateSuccess method [Microsoft TV Technologies], CertificateSuccess method [Microsoft TV Technologies],IMSVidStreamBufferSinkEvent interface, IMSVidStreamBufferSinkEvent interface [Microsoft TV Technologies],CertificateSuccess method, IMSVidStreamBufferSinkEvent.CertificateSuccess, IMSVidStreamBufferSinkEvent::CertificateSuccess, IMSVidStreamBufferSinkEventCertificateSuccess, mstv.imsvidstreambuffersinkevent_certificatesuccess, segment/IMSVidStreamBufferSinkEvent::CertificateSuccess
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidStreamBufferSinkEvent::CertificateSuccess
 - segment/IMSVidStreamBufferSinkEvent::CertificateSuccess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSinkEvent.CertificateSuccess
---

# IMSVidStreamBufferSinkEvent::CertificateSuccess


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP Service Pack 1 or later.
        



The <b>CertificateSuccess</b> method is called when the object succeeds in getting an encryption/decryption license. The method is called only if an earlier failure occurred.



## -returns

Return S_OK or an error code.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersinkevent">IMSVidStreamBufferSinkEvent Interface</a>
