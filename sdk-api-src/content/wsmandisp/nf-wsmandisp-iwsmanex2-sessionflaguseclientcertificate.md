---
UID: NF:wsmandisp.IWSManEx2.SessionFlagUseClientCertificate
title: IWSManEx2::SessionFlagUseClientCertificate (wsmandisp.h)
description: Returns the value of the authentication flag WSManFlagUseClientCertificate for use in the flags parameter of IWSMan::CreateSession.
helpviewer_keywords: ["IWSManEx2 interface [Windows Remote Management]","SessionFlagUseClientCertificate method","IWSManEx2.SessionFlagUseClientCertificate","IWSManEx2::SessionFlagUseClientCertificate","SessionFlagUseClientCertificate","SessionFlagUseClientCertificate method [Windows Remote Management]","SessionFlagUseClientCertificate method [Windows Remote Management]","IWSManEx2 interface","winrm.iwsmanex2_sessionflaguseclientcertificate","wsmandisp/IWSManEx2::SessionFlagUseClientCertificate"]
old-location: winrm\iwsmanex2_sessionflaguseclientcertificate.htm
tech.root: winrm
ms.assetid: 287e17b4-ca2f-4816-af26-b76b4e717c70
ms.date: 12/05/2018
ms.keywords: IWSManEx2 interface [Windows Remote Management],SessionFlagUseClientCertificate method, IWSManEx2.SessionFlagUseClientCertificate, IWSManEx2::SessionFlagUseClientCertificate, SessionFlagUseClientCertificate, SessionFlagUseClientCertificate method [Windows Remote Management], SessionFlagUseClientCertificate method [Windows Remote Management],IWSManEx2 interface, winrm.iwsmanex2_sessionflaguseclientcertificate, wsmandisp/IWSManEx2::SessionFlagUseClientCertificate
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSManEx2::SessionFlagUseClientCertificate
 - wsmandisp/IWSManEx2::SessionFlagUseClientCertificate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEx2.SessionFlagUseClientCertificate
---

# IWSManEx2::SessionFlagUseClientCertificate


## -description

Returns the value of the authentication flag <b>WSManFlagUseClientCertificate</b> for use in the <i>flags</i> parameter of <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

<b>WSManFlagUseClientCertificate</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="/windows/desktop/WinRM/authentication-constants">Authentication Constants</a>.

## -parameters

### -param flags [out]

The session flags to use.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex2">IWSManEx2</a>