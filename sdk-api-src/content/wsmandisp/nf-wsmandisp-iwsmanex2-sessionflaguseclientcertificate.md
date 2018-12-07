---
UID: NF:wsmandisp.IWSManEx2.SessionFlagUseClientCertificate
title: IWSManEx2::SessionFlagUseClientCertificate
author: windows-sdk-content
description: Returns the value of the authentication flag WSManFlagUseClientCertificate for use in the flags parameter of IWSMan::CreateSession.
old-location: winrm\iwsmanex2_sessionflaguseclientcertificate.htm
tech.root: winrm
ms.assetid: 287e17b4-ca2f-4816-af26-b76b4e717c70
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSManEx2 interface [Windows Remote Management],SessionFlagUseClientCertificate method, IWSManEx2.SessionFlagUseClientCertificate, IWSManEx2::SessionFlagUseClientCertificate, SessionFlagUseClientCertificate, SessionFlagUseClientCertificate method [Windows Remote Management], SessionFlagUseClientCertificate method [Windows Remote Management],IWSManEx2 interface, winrm.iwsmanex2_sessionflaguseclientcertificate, wsmandisp/IWSManEx2::SessionFlagUseClientCertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSManEx2::SessionFlagUseClientCertificate


## -description


Returns the value of the authentication flag <b>WSManFlagUseClientCertificate</b> for use in the <i>flags</i> parameter of <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

<b>WSManFlagUseClientCertificate</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="https://msdn.microsoft.com/adfefbc9-c386-48db-a0c2-145aa4f91bfa">Authentication Constants</a>.


## -parameters




### -param flags [out]

The session flags to use.


## -see-also




<a href="https://msdn.microsoft.com/4c398e10-3822-4042-8a43-1d7889ae6cac">IWSManEx2</a>
 

 

