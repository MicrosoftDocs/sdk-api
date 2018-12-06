---
UID: NF:wsmandisp.IWSManEx.SessionFlagUseNoAuthentication
title: IWSManEx::SessionFlagUseNoAuthentication
author: windows-sdk-content
description: Returns the value of the authentication flag WSManFlagUseNoAuthentication for use in the flags parameter of IWSMan::CreateSession.
old-location: winrm\iwsmanex_sessionflagusenoauthentication.htm
tech.root: winrm
ms.assetid: af3f7512-c1d5-4c4d-b79a-b0bf8b95be6d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagUseNoAuthentication method, IWSManEx.SessionFlagUseNoAuthentication, IWSManEx::SessionFlagUseNoAuthentication, SessionFlagUseNoAuthentication, SessionFlagUseNoAuthentication method [Windows Remote Management], SessionFlagUseNoAuthentication method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagusenoauthentication, wsmandisp/IWSManEx::SessionFlagUseNoAuthentication
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
 - IWSManEx.SessionFlagUseNoAuthentication
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSManEx::SessionFlagUseNoAuthentication


## -description


The 
    <a href="https://msdn.microsoft.com/22a8107a-8e5e-4636-bf7d-a261f885e074">WSMan.SessionFlagUseNoAuthentication</a> 
    method returns the value of the authentication flag 
    <b>WSManFlagUseNoAuthentication</b> for use in the <i>flags</i> parameter of 
    <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

<b>WSManFlagUseNoAuthentication</b> is a constant in the 
    <b>__WSManSessionFlags</b> enumeration. For more information, see 
    <a href="https://msdn.microsoft.com/adfefbc9-c386-48db-a0c2-145aa4f91bfa">Authentication Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/22a8107a-8e5e-4636-bf7d-a261f885e074">WSMan.SessionFlagUseNoAuthentication</a>
 

 

