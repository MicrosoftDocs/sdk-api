---
UID: NF:wsmandisp.IWSManEx.SessionFlagCredUsernamePassword
title: IWSManEx::SessionFlagCredUsernamePassword (wsmandisp.h)
description: Returns the value of the authentication flag WSManFlagCredUsernamePassword for use in the flags parameter of IWSMan::CreateSession.
helpviewer_keywords: ["IWSManEx interface [Windows Remote Management]","SessionFlagCredUsernamePassword method","IWSManEx.SessionFlagCredUsernamePassword","IWSManEx::SessionFlagCredUsernamePassword","SessionFlagCredUsernamePassword","SessionFlagCredUsernamePassword method [Windows Remote Management]","SessionFlagCredUsernamePassword method [Windows Remote Management]","IWSManEx interface","winrm.iwsmanex_sessionflagcredusernamepassword","wsmandisp/IWSManEx::SessionFlagCredUsernamePassword"]
old-location: winrm\iwsmanex_sessionflagcredusernamepassword.htm
tech.root: winrm
ms.assetid: e9af95ac-4543-4d8b-ac6e-15e89b73713e
ms.date: 12/05/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagCredUsernamePassword method, IWSManEx.SessionFlagCredUsernamePassword, IWSManEx::SessionFlagCredUsernamePassword, SessionFlagCredUsernamePassword, SessionFlagCredUsernamePassword method [Windows Remote Management], SessionFlagCredUsernamePassword method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagcredusernamepassword, wsmandisp/IWSManEx::SessionFlagCredUsernamePassword
f1_keywords:
- wsmandisp/IWSManEx.SessionFlagCredUsernamePassword
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
- IWSManEx.SessionFlagCredUsernamePassword
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManEx::SessionFlagCredUsernamePassword


## -description


The <b>IWSMan.SessionFlagCredUsernamePassword</b> method returns the value of the authentication flag <b>WSManFlagCredUsernamePassword</b> for use in the <i>flags</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

<b>WSManFlagCredUsernamePassword</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinRM/authentication-constants">Authentication Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman-sessionflagcredusernamepassword">WSMan.SessionFlagCredUsernamePassword</a>
 

 

