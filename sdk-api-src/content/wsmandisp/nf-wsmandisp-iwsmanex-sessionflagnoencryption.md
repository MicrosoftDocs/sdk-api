---
UID: NF:wsmandisp.IWSManEx.SessionFlagNoEncryption
title: IWSManEx::SessionFlagNoEncryption (wsmandisp.h)
description: Returns the value of the authentication flag WSManFlagNoEncryption for use in the flags parameter of IWSMan::CreateSession.
helpviewer_keywords: ["IWSManEx interface [Windows Remote Management]","SessionFlagNoEncryption method","IWSManEx.SessionFlagNoEncryption","IWSManEx::SessionFlagNoEncryption","SessionFlagNoEncryption","SessionFlagNoEncryption method [Windows Remote Management]","SessionFlagNoEncryption method [Windows Remote Management]","IWSManEx interface","winrm.iwsmanex_sessionflagnoencryption","wsmandisp/IWSManEx::SessionFlagNoEncryption"]
old-location: winrm\iwsmanex_sessionflagnoencryption.htm
tech.root: winrm
ms.assetid: ec96e873-ecb6-4d89-ada3-41c889544091
ms.date: 12/05/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagNoEncryption method, IWSManEx.SessionFlagNoEncryption, IWSManEx::SessionFlagNoEncryption, SessionFlagNoEncryption, SessionFlagNoEncryption method [Windows Remote Management], SessionFlagNoEncryption method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagnoencryption, wsmandisp/IWSManEx::SessionFlagNoEncryption
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
 - IWSManEx::SessionFlagNoEncryption
 - wsmandisp/IWSManEx::SessionFlagNoEncryption
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
 - IWSManEx.SessionFlagNoEncryption
---

# IWSManEx::SessionFlagNoEncryption


## -description

The <a href="/windows/desktop/WinRM/wsman-sessionflagnoencryption">WSMan.SessionFlagNoEncryption</a> method returns the value of the authentication flag <b>WSManFlagNoEncryption</b> for use in the <i>flags</i> parameter of <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

<b>WSManFlagNoEncryption</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="/windows/desktop/WinRM/other-session-constants">Other Session Constants</a>.

## -parameters

### -param flags [out]

The value of the constant.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="/windows/desktop/WinRM/wsman-sessionflagnoencryption">WSMan.SessionFlagNoEncryption</a>