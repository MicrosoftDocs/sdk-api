---
UID: NF:wsmandisp.IWSManEx.EnumerationFlagReturnObjectAndEPR
title: IWSManEx::EnumerationFlagReturnObjectAndEPR (wsmandisp.h)
description: Returns the value of the enumeration constant EnumerationFlagReturnObjectAndEPR for use in the flags parameter of the IWSManSession::Enumerate method.
helpviewer_keywords: ["EnumerationFlagReturnObjectAndEPR","EnumerationFlagReturnObjectAndEPR method [Windows Remote Management]","EnumerationFlagReturnObjectAndEPR method [Windows Remote Management]","IWSManEx interface","IWSManEx interface [Windows Remote Management]","EnumerationFlagReturnObjectAndEPR method","IWSManEx.EnumerationFlagReturnObjectAndEPR","IWSManEx::EnumerationFlagReturnObjectAndEPR","winrm.iwsmanex_enumerationflagreturnobjectandepr","wsmandisp/IWSManEx::EnumerationFlagReturnObjectAndEPR"]
old-location: winrm\iwsmanex_enumerationflagreturnobjectandepr.htm
tech.root: winrm
ms.assetid: 3ded5083-5f4a-4e07-96d6-7856c0a2f340
ms.date: 12/05/2018
ms.keywords: EnumerationFlagReturnObjectAndEPR, EnumerationFlagReturnObjectAndEPR method [Windows Remote Management], EnumerationFlagReturnObjectAndEPR method [Windows Remote Management],IWSManEx interface, IWSManEx interface [Windows Remote Management],EnumerationFlagReturnObjectAndEPR method, IWSManEx.EnumerationFlagReturnObjectAndEPR, IWSManEx::EnumerationFlagReturnObjectAndEPR, winrm.iwsmanex_enumerationflagreturnobjectandepr, wsmandisp/IWSManEx::EnumerationFlagReturnObjectAndEPR
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
 - IWSManEx::EnumerationFlagReturnObjectAndEPR
 - wsmandisp/IWSManEx::EnumerationFlagReturnObjectAndEPR
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
 - IWSManEx.EnumerationFlagReturnObjectAndEPR
---

# IWSManEx::EnumerationFlagReturnObjectAndEPR


## -description

The <b>IWSManEx::EnumerationFlagReturnObjectAndEPR</b> method returns the value of the enumeration constant <b>EnumerationFlagReturnObjectAndEPR</b> for use in the <i>flags</i> parameter of the <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

<b>EnumerationFlagReturnObjectAndEPR</b> is a constant in the <b>_WSManEnumFlags</b> enumeration and is described in <a href="/windows/desktop/WinRM/enumeration-constants">Enumeration Constants</a>.

## -parameters

### -param flags [out]

The value of the constant.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>