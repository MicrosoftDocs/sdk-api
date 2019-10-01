---
UID: NF:wsmandisp.IWSManEx2.SessionFlagUseClientCertificate
title: IWSManEx2::SessionFlagUseClientCertificate (wsmandisp.h)
author: windows-sdk-content
description: Returns the value of the authentication flag WSManFlagUseClientCertificate for use in the flags parameter of IWSMan::CreateSession.
old-location: winrm\iwsmanex2_sessionflaguseclientcertificate.htm
tech.root: winrm
ms.assetid: 287e17b4-ca2f-4816-af26-b76b4e717c70
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSManEx2 interface [Windows Remote Management],SessionFlagUseClientCertificate method, IWSManEx2.SessionFlagUseClientCertificate, IWSManEx2::SessionFlagUseClientCertificate, SessionFlagUseClientCertificate, SessionFlagUseClientCertificate method [Windows Remote Management], SessionFlagUseClientCertificate method [Windows Remote Management],IWSManEx2 interface, winrm.iwsmanex2_sessionflaguseclientcertificate, wsmandisp/IWSManEx2::SessionFlagUseClientCertificate
ms.topic: method
f1_keywords: 
 - "wsmandisp/IWSManEx2.SessionFlagUseClientCertificate"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEx2.SessionFlagUseClientCertificate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManEx2::SessionFlagUseClientCertificate


## -description


Returns the value of the authentication flag <b>WSManFlagUseClientCertificate</b> for use in the <i>flags</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

<b>WSManFlagUseClientCertificate</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinRM/authentication-constants">Authentication Constants</a>.


## -parameters




### -param flags [out]

The session flags to use.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex2">IWSManEx2</a>
 

 

