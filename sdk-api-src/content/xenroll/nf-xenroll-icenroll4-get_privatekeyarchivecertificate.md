---
UID: NF:xenroll.ICEnroll4.get_PrivateKeyArchiveCertificate
title: ICEnroll4::get_PrivateKeyArchiveCertificate (xenroll.h)
description: Sets or retrieves the certificate that is used to archive a private key with a PKCS (Get)
helpviewer_keywords: ["CEnroll object [Security]","PrivateKeyArchiveCertificate property","ICEnroll4 interface [Security]","PrivateKeyArchiveCertificate property","ICEnroll4.PrivateKeyArchiveCertificate","ICEnroll4.get_PrivateKeyArchiveCertificate","ICEnroll4::PrivateKeyArchiveCertificate","ICEnroll4::get_PrivateKeyArchiveCertificate","ICEnroll4::put_PrivateKeyArchiveCertificate","PrivateKeyArchiveCertificate property [Security]","PrivateKeyArchiveCertificate property [Security]","CEnroll object","PrivateKeyArchiveCertificate property [Security]","ICEnroll4 interface","_xen_icenroll4_privatekeyarchivecertificate","get_PrivateKeyArchiveCertificate","security.icenroll4_privatekeyarchivecertificate","xenroll/ICEnroll4::PrivateKeyArchiveCertificate","xenroll/ICEnroll4::get_PrivateKeyArchiveCertificate","xenroll/ICEnroll4::put_PrivateKeyArchiveCertificate"]
old-location: security\icenroll4_privatekeyarchivecertificate.htm
tech.root: security
ms.assetid: c5099bef-2882-4106-a2e6-a144e16993c3
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],PrivateKeyArchiveCertificate property, ICEnroll4 interface [Security],PrivateKeyArchiveCertificate property, ICEnroll4.PrivateKeyArchiveCertificate, ICEnroll4.get_PrivateKeyArchiveCertificate, ICEnroll4::PrivateKeyArchiveCertificate, ICEnroll4::get_PrivateKeyArchiveCertificate, ICEnroll4::put_PrivateKeyArchiveCertificate, PrivateKeyArchiveCertificate property [Security], PrivateKeyArchiveCertificate property [Security],CEnroll object, PrivateKeyArchiveCertificate property [Security],ICEnroll4 interface, _xen_icenroll4_privatekeyarchivecertificate, get_PrivateKeyArchiveCertificate, security.icenroll4_privatekeyarchivecertificate, xenroll/ICEnroll4::PrivateKeyArchiveCertificate, xenroll/ICEnroll4::get_PrivateKeyArchiveCertificate, xenroll/ICEnroll4::put_PrivateKeyArchiveCertificate
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
 - ICEnroll4::get_PrivateKeyArchiveCertificate
 - xenroll/ICEnroll4::get_PrivateKeyArchiveCertificate
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
 - ICEnroll4.PrivateKeyArchiveCertificate
 - ICEnroll4.get_PrivateKeyArchiveCertificate
 - ICEnroll4.put_PrivateKeyArchiveCertificate
 - CEnroll.PrivateKeyArchiveCertificate
---

# ICEnroll4::get_PrivateKeyArchiveCertificate


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>PrivateKeyArchiveCertificate</b> property sets or retrieves the certificate that is used to archive a private key with a PKCS #7 or <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) request.

If this property is not null, the <a href="/windows/desktop/SecGloss/p-gly">private key</a> is encrypted based on the specified certificate and added to the request as an unauthenticated <a href="/windows/desktop/SecGloss/a-gly">attribute</a>. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

This property is read/write.

## -parameters
