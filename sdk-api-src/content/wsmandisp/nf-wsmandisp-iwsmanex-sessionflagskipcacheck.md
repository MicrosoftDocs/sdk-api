---
UID: NF:wsmandisp.IWSManEx.SessionFlagSkipCACheck
title: IWSManEx::SessionFlagSkipCACheck (wsmandisp.h)
description: Returns the value of the WSManFlagSkipCACheck authentication flag for use in the flags parameter of the IWSMan::CreateSession method.
helpviewer_keywords: ["IWSManEx interface [Windows Remote Management]","SessionFlagSkipCACheck method","IWSManEx.SessionFlagSkipCACheck","IWSManEx::SessionFlagSkipCACheck","SessionFlagSkipCACheck","SessionFlagSkipCACheck method [Windows Remote Management]","SessionFlagSkipCACheck method [Windows Remote Management]","IWSManEx interface","winrm.iwsmanex_sessionflagskipcacheck","wsmandisp/IWSManEx::SessionFlagSkipCACheck"]
old-location: winrm\iwsmanex_sessionflagskipcacheck.htm
tech.root: winrm
ms.assetid: 683054fd-7ee3-4c90-a5cd-234e7d60349d
ms.date: 12/05/2018
ms.keywords: IWSManEx interface [Windows Remote Management],SessionFlagSkipCACheck method, IWSManEx.SessionFlagSkipCACheck, IWSManEx::SessionFlagSkipCACheck, SessionFlagSkipCACheck, SessionFlagSkipCACheck method [Windows Remote Management], SessionFlagSkipCACheck method [Windows Remote Management],IWSManEx interface, winrm.iwsmanex_sessionflagskipcacheck, wsmandisp/IWSManEx::SessionFlagSkipCACheck
f1_keywords:
- wsmandisp/IWSManEx.SessionFlagSkipCACheck
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
- IWSManEx.SessionFlagSkipCACheck
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManEx::SessionFlagSkipCACheck


## -description


The <a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman-sessionflagskipcacheck">WSMan.SessionFlagSkipCACheck</a> method returns the value of the  <b>WSManFlagSkipCACheck</b> authentication flag for use in the <i>flags</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsman-createsession">IWSMan::CreateSession</a> method.

<b>WSManFlagSkipCACheck</b> is a constant in the <b>__WSManSessionFlags</b> enumeration. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinRM/authentication-constants">Authentication Constants</a>.


## -parameters




### -param flags [out]

The value of the constant.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman-sessionflagskipcacheck">WSMan.SessionFlagSkipCACheck</a>
 

 

