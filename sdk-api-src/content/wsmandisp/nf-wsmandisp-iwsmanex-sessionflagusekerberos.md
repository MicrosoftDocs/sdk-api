---
UID: NF:wsmandisp.IWSManEx.SessionFlagUseKerberos
title: IWSManEx::SessionFlagUseKerberos
author: windows-sdk-content
description: Returns the value of the authentication flag WSManFlagUseKerberos for use in the flags parameter of IWSMan::CreateSession.
old-location: winrm\iwsmanex_sessionflagusekerberos.htm
old-project: WinRM
ms.assetid: 14b949d8-774b-4224-ab08-b52ff71ab1bb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagUseKerberos method, IWSManEx.SessionFlagUseKerberos, IWSManEx::SessionFlagUseKerberos, SessionFlagUseKerberos, SessionFlagUseKerberos method [Windows Remote Management], SessionFlagUseKerberos method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagusekerberos, wsmandisp/IWSManEx::SessionFlagUseKerberos
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.redist: 
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
 - IWSManEx.SessionFlagUseKerberos
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManEx::SessionFlagUseKerberos


## -description


The <a href="https://msdn.microsoft.com/be005312-1e87-4371-9791-709a9be46f7c">WSMan.WSMan.SessionFlagUseKerberos</a> method returns the value of the authentication flag <b>WSManFlagUseKerberos</b> for use in the <i>flags</i> parameter of <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

<b>WSManFlagUseKerberos</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="https://msdn.microsoft.com/adfefbc9-c386-48db-a0c2-145aa4f91bfa">Authentication Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/be005312-1e87-4371-9791-709a9be46f7c">WSMan.WSMan.SessionFlagUseKerberos</a>
 

 

