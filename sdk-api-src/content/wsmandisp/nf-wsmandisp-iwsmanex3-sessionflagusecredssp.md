---
UID: NF:wsmandisp.IWSManEx3.SessionFlagUseCredSsp
title: IWSManEx3::SessionFlagUseCredSsp (wsmandisp.h)
description: Returns the value of the authentication flag WSManFlagUseCredSsp for use in the flags parameter of IWSMan::CreateSession.
helpviewer_keywords: ["IWSManEx3 interface [Windows Remote Management]","SessionFlagUseCredSsp method","IWSManEx3.SessionFlagUseCredSsp","IWSManEx3::SessionFlagUseCredSsp","SessionFlagUseCredSsp","SessionFlagUseCredSsp method [Windows Remote Management]","SessionFlagUseCredSsp method [Windows Remote Management]","IWSManEx3 interface","winrm.iwsmanex3_sessionflagusecredssp","wsmandisp/IWSManEx3::SessionFlagUseCredSsp"]
old-location: winrm\iwsmanex3_sessionflagusecredssp.htm
tech.root: winrm
ms.assetid: 69c62ad1-319e-4716-a2c7-61b931567244
ms.date: 12/05/2018
ms.keywords: IWSManEx3 interface [Windows Remote Management],SessionFlagUseCredSsp method, IWSManEx3.SessionFlagUseCredSsp, IWSManEx3::SessionFlagUseCredSsp, SessionFlagUseCredSsp, SessionFlagUseCredSsp method [Windows Remote Management], SessionFlagUseCredSsp method [Windows Remote Management],IWSManEx3 interface, winrm.iwsmanex3_sessionflagusecredssp, wsmandisp/IWSManEx3::SessionFlagUseCredSsp
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - IWSManEx3::SessionFlagUseCredSsp
 - wsmandisp/IWSManEx3::SessionFlagUseCredSsp
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
 - IWSManEx3.SessionFlagUseCredSsp
---

# IWSManEx3::SessionFlagUseCredSsp


## -description

Returns the value of the authentication flag <b>WSManFlagUseCredSsp</b> for use in the <i>flags</i> parameter of <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a>.

<b>WSManFlagUseCredSsp</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="/windows/desktop/WinRM/authentication-constants">Authentication Constants</a>.

## -parameters

### -param flags [out, retval]

Specifies the authentication flag to use.

## -returns

If the method succeeds, it returns the authentication flag. Otherwise, it returns an HRESULT error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex3">IWSManEx3</a>