---
UID: NF:xenroll.ICEnroll4.put_PrivateKeyArchiveCertificate
title: ICEnroll4::put_PrivateKeyArchiveCertificate
author: windows-sdk-content
description: Sets or retrieves the certificate that is used to archive a private key with a PKCS #7 or Certificate Management over CMS (CMC) request.
old-location: security\icenroll4_privatekeyarchivecertificate.htm
tech.root: seccrypto
ms.assetid: c5099bef-2882-4106-a2e6-a144e16993c3
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CEnroll object [Security],PrivateKeyArchiveCertificate property, ICEnroll4 interface [Security],PrivateKeyArchiveCertificate property, ICEnroll4.PrivateKeyArchiveCertificate, ICEnroll4.put_PrivateKeyArchiveCertificate, ICEnroll4::PrivateKeyArchiveCertificate, ICEnroll4::get_PrivateKeyArchiveCertificate, ICEnroll4::put_PrivateKeyArchiveCertificate, PrivateKeyArchiveCertificate property [Security], PrivateKeyArchiveCertificate property [Security],CEnroll object, PrivateKeyArchiveCertificate property [Security],ICEnroll4 interface, _xen_icenroll4_privatekeyarchivecertificate, put_PrivateKeyArchiveCertificate, security.icenroll4_privatekeyarchivecertificate, xenroll/ICEnroll4::PrivateKeyArchiveCertificate, xenroll/ICEnroll4::get_PrivateKeyArchiveCertificate, xenroll/ICEnroll4::put_PrivateKeyArchiveCertificate
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll4::put_PrivateKeyArchiveCertificate


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>PrivateKeyArchiveCertificate</b> property sets or retrieves the certificate that is used to archive a private key with a PKCS #7 or <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Management over CMS</a> (CMC) request.

If this property is not null, the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> is encrypted based on the specified certificate and added to the request as an unauthenticated <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a>. This property was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.

This property is read/write.


## -parameters

