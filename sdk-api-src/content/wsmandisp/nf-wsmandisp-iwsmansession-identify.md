---
UID: NF:wsmandisp.IWSManSession.Identify
title: IWSManSession::Identify
author: windows-sdk-content
description: Queries a remote computer to determine if it supports the WS-Management protocol.
old-location: winrm\iwsmansession_identify.htm
old-project: winrm
ms.assetid: d3f4e33e-436b-4f05-8696-321a3bfbacd5
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IWSManSession interface [Windows Remote Management],Identify method, IWSManSession.Identify, IWSManSession::Identify, Identify, Identify method [Windows Remote Management], Identify method [Windows Remote Management],IWSManSession interface, winrm.iwsmansession_identify, wsmandisp/IWSManSession::Identify
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSManProxyAuthenticationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManSession.Identify
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManSession::Identify


## -description


The <b>IWSManSession::Identify</b> method queries a remote computer to determine if it supports the WS-Management protocol. For more information, see <a href="https://msdn.microsoft.com/4d11ac02-fa8b-45d7-bceb-a18f561bc928">Detecting Whether a Remote Computer Supports WS-Management Protocol</a>.


## -parameters




### -param flags [in, optional]

The only flag that is accepted is <b>WSManFlagUseNoAuthentication</b>.


### -param result [out]

A value that, upon success, is an XML string that specifies the WS-Management protocol version, the operating system vendor and, if the request was sent authenticated, the operating system version.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a>



<a href="https://msdn.microsoft.com/b86ec9b8-8fc4-4c3e-aca7-2f7d039749df">Session.Identify</a>
 

 

