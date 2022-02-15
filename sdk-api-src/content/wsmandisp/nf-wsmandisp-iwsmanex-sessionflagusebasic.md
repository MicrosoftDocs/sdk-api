---
UID: NF:wsmandisp.IWSManEx.SessionFlagUseBasic
title: IWSManEx::SessionFlagUseBasic (wsmandisp.h)
description: Returns the value of the authentication flag WSManFlagUseBasic for use in the flags parameter of IWSMan::CreateSession.
helpviewer_keywords: ["IWSManEx interface [Windows Remote Management]","SessionFlagUseBasic method","IWSManEx.SessionFlagUseBasic","IWSManEx::SessionFlagUseBasic","SessionFlagUseBasic","SessionFlagUseBasic method [Windows Remote Management]","SessionFlagUseBasic method [Windows Remote Management]","IWSManEx interface","winrm.iwsmanex_sessionflagusebasic","wsmandisp/IWSManEx::SessionFlagUseBasic"]
old-location: winrm\iwsmanex_sessionflagusebasic.htm
tech.root: winrm
ms.assetid: 6b7457e2-1c19-4b33-bb38-5068f3c295cb
ms.date: 12/05/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagUseBasic method, IWSManEx.SessionFlagUseBasic, IWSManEx::SessionFlagUseBasic, SessionFlagUseBasic, SessionFlagUseBasic method [Windows Remote Management], SessionFlagUseBasic method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagusebasic, wsmandisp/IWSManEx::SessionFlagUseBasic
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
 - IWSManEx::SessionFlagUseBasic
 - wsmandisp/IWSManEx::SessionFlagUseBasic
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
 - IWSManEx.SessionFlagUseBasic
---

# IWSManEx::SessionFlagUseBasic


## -description

The <a href="/windows/desktop/WinRM/wsman-sessionflagusebasic">WSMan.SessionFlagUseBasic</a> method returns the value of the authentication flag <b>WSManFlagUseBasic</b> for use in the <i>flags</i> parameter of <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

<b>WSManFlagUseBasic</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="/windows/desktop/WinRM/authentication-constants">Authentication Constants</a>.

## -parameters

### -param flags [out]

The value of the constant.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="/windows/desktop/WinRM/wsman-sessionflagusebasic">WSMan.SessionFlagUseBasic</a>