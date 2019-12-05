---
UID: NF:wsmandisp.IWSManSession.Identify
title: IWSManSession::Identify (wsmandisp.h)
description: Queries a remote computer to determine if it supports the WS-Management protocol.
old-location: winrm\iwsmansession_identify.htm
tech.root: winrm
ms.assetid: d3f4e33e-436b-4f05-8696-321a3bfbacd5
ms.date: 12/05/2018
ms.keywords: IWSManSession interface [Windows Remote Management],Identify method, IWSManSession.Identify, IWSManSession::Identify, Identify, Identify method [Windows Remote Management], Identify method [Windows Remote Management],IWSManSession interface, winrm.iwsmansession_identify, wsmandisp/IWSManSession::Identify
ms.topic: method
f1_keywords:
- wsmandisp/IWSManSession.Identify
dev_langs:
- c++
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
- IWSManSession.Identify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManSession::Identify


## -description


The <b>IWSManSession::Identify</b> method queries a remote computer to determine if it supports the WS-Management protocol. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinRM/detecting-whether-a-remote-computer-supports-ws-management-protocol">Detecting Whether a Remote Computer Supports WS-Management Protocol</a>.


## -parameters




### -param flags [in, optional]

The only flag that is accepted is <b>WSManFlagUseNoAuthentication</b>.


### -param result [out]

A value that, upon success, is an XML string that specifies the WS-Management protocol version, the operating system vendor and, if the request was sent authenticated, the operating system version.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/session-identify">Session.Identify</a>
 

 

