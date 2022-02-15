---
UID: NF:wsmandisp.IWSManEx.SessionFlagUTF8
title: IWSManEx::SessionFlagUTF8 (wsmandisp.h)
description: Returns the value of the authentication flag WSManFlagUTF8 for use in the flags parameter of IWSMan::CreateSession.
helpviewer_keywords: ["IWSManEx interface [Windows Remote Management]","SessionFlagUTF8 method","IWSManEx.SessionFlagUTF8","IWSManEx::SessionFlagUTF8","SessionFlagUTF8","SessionFlagUTF8 method [Windows Remote Management]","SessionFlagUTF8 method [Windows Remote Management]","IWSManEx interface","winrm.iwsmanex_sessionflagutf8","wsmandisp/IWSManEx::SessionFlagUTF8"]
old-location: winrm\iwsmanex_sessionflagutf8.htm
tech.root: winrm
ms.assetid: 99c96057-fbd7-4d8c-a204-1660f84d640f
ms.date: 12/05/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagUTF8 method, IWSManEx.SessionFlagUTF8, IWSManEx::SessionFlagUTF8, SessionFlagUTF8, SessionFlagUTF8 method [Windows Remote Management], SessionFlagUTF8 method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagutf8, wsmandisp/IWSManEx::SessionFlagUTF8
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
 - IWSManEx::SessionFlagUTF8
 - wsmandisp/IWSManEx::SessionFlagUTF8
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
 - IWSManEx.SessionFlagUTF8
---

# IWSManEx::SessionFlagUTF8


## -description

The <a href="/windows/desktop/WinRM/wsman-sessionflagutf8">WSMan.SessionFlagUTF8</a> method returns the value of the authentication flag <b>WSManFlagUTF8</b> for use in the <i>flags</i> parameter of <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

<b>WSManFlagUTF8</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="/windows/desktop/WinRM/other-session-constants">Other Session Constants</a>.

## -parameters

### -param flags [out]

The value of the constant.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="/windows/desktop/WinRM/wsman-sessionflagutf8">WSMan.SessionFlagUTF8</a>