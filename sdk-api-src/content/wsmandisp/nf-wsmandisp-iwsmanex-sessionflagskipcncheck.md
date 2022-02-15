---
UID: NF:wsmandisp.IWSManEx.SessionFlagSkipCNCheck
title: IWSManEx::SessionFlagSkipCNCheck (wsmandisp.h)
description: Returns the value of the authentication flag WSManFlagSkipCNCheck for use in the flags parameter of IWSMan::CreateSession.
helpviewer_keywords: ["IWSManEx interface [Windows Remote Management]","SessionFlagSkipCNCheck method","IWSManEx.SessionFlagSkipCNCheck","IWSManEx::SessionFlagSkipCNCheck","SessionFlagSkipCNCheck","SessionFlagSkipCNCheck method [Windows Remote Management]","SessionFlagSkipCNCheck method [Windows Remote Management]","IWSManEx interface","winrm.iwsmanex_sessionflagskipcncheck","wsmandisp/IWSManEx::SessionFlagSkipCNCheck"]
old-location: winrm\iwsmanex_sessionflagskipcncheck.htm
tech.root: winrm
ms.assetid: cf364e3a-e532-48cf-9b88-fdc661e70ffa
ms.date: 12/05/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagSkipCNCheck method, IWSManEx.SessionFlagSkipCNCheck, IWSManEx::SessionFlagSkipCNCheck, SessionFlagSkipCNCheck, SessionFlagSkipCNCheck method [Windows Remote Management], SessionFlagSkipCNCheck method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagskipcncheck, wsmandisp/IWSManEx::SessionFlagSkipCNCheck
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
 - IWSManEx::SessionFlagSkipCNCheck
 - wsmandisp/IWSManEx::SessionFlagSkipCNCheck
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
 - IWSManEx.SessionFlagSkipCNCheck
---

# IWSManEx::SessionFlagSkipCNCheck


## -description

The <a href="/windows/desktop/WinRM/wsman-sessionflagskipcncheck">WSMan.SessionFlagSkipCNCheck</a> method returns the value of the authentication flag <b>WSManFlagSkipCNCheck</b> for use in the <i>flags</i> parameter of <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

<b>WSManFlagSkipCNCheck</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="/windows/desktop/WinRM/authentication-constants">Authentication Constants</a>.

## -parameters

### -param flags [out]

The value of the constant.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="/windows/desktop/WinRM/wsman-sessionflagskipcncheck">WSMan.SessionFlagSkipCNCheck</a>