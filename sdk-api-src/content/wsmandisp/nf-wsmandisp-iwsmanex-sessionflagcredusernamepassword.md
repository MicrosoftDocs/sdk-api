---
UID: NF:wsmandisp.IWSManEx.SessionFlagCredUsernamePassword
title: IWSManEx::SessionFlagCredUsernamePassword
author: windows-sdk-content
description: Returns the value of the authentication flag WSManFlagCredUsernamePassword for use in the flags parameter of IWSMan::CreateSession.
old-location: winrm\iwsmanex_sessionflagcredusernamepassword.htm
old-project: WinRM
ms.assetid: e9af95ac-4543-4d8b-ac6e-15e89b73713e
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagCredUsernamePassword method, IWSManEx.SessionFlagCredUsernamePassword, IWSManEx::SessionFlagCredUsernamePassword, SessionFlagCredUsernamePassword, SessionFlagCredUsernamePassword method [Windows Remote Management], SessionFlagCredUsernamePassword method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagcredusernamepassword, wsmandisp/IWSManEx::SessionFlagCredUsernamePassword
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
 - IWSManEx.SessionFlagCredUsernamePassword
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManEx::SessionFlagCredUsernamePassword


## -description


The <b>IWSMan.SessionFlagCredUsernamePassword</b> method returns the value of the authentication flag <b>WSManFlagCredUsernamePassword</b> for use in the <i>flags</i> parameter of <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

<b>WSManFlagCredUsernamePassword</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="https://msdn.microsoft.com/adfefbc9-c386-48db-a0c2-145aa4f91bfa">Authentication Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/70d12df4-f0ac-499a-8b2f-6ba83b77869e">WSMan.SessionFlagCredUsernamePassword</a>
 

 

