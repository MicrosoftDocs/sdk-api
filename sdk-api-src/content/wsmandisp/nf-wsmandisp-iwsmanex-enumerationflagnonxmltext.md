---
UID: NF:wsmandisp.IWSManEx.EnumerationFlagNonXmlText
title: IWSManEx::EnumerationFlagNonXmlText (wsmandisp.h)
description: Returns the value of the enumeration constant WSManFlagNonXmlText for use in the flags parameter of the IWSManSession::Enumerate method.
helpviewer_keywords: ["EnumerationFlagNonXmlText","EnumerationFlagNonXmlText method [Windows Remote Management]","EnumerationFlagNonXmlText method [Windows Remote Management]","IWSManEx interface","IWSManEx interface [Windows Remote Management]","EnumerationFlagNonXmlText method","IWSManEx.EnumerationFlagNonXmlText","IWSManEx::EnumerationFlagNonXmlText","winrm.iwsmanex_enumerationflagnonxmltext","wsmandisp/IWSManEx::EnumerationFlagNonXmlText"]
old-location: winrm\iwsmanex_enumerationflagnonxmltext.htm
tech.root: winrm
ms.assetid: f94dc9cc-a4c5-44b8-9ace-63b80b1087d2
ms.date: 12/05/2018
ms.keywords: EnumerationFlagNonXmlText, EnumerationFlagNonXmlText method [Windows Remote Management], EnumerationFlagNonXmlText method [Windows Remote Management],IWSManEx interface, IWSManEx interface [Windows Remote Management],EnumerationFlagNonXmlText method, IWSManEx.EnumerationFlagNonXmlText, IWSManEx::EnumerationFlagNonXmlText, winrm.iwsmanex_enumerationflagnonxmltext, wsmandisp/IWSManEx::EnumerationFlagNonXmlText
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
 - IWSManEx::EnumerationFlagNonXmlText
 - wsmandisp/IWSManEx::EnumerationFlagNonXmlText
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
 - IWSManEx.EnumerationFlagNonXmlText
---

# IWSManEx::EnumerationFlagNonXmlText


## -description

The 
    <b>IWSManEx::EnumerationFlagNonXmlText</b> 
    method returns the value of the enumeration constant <b>WSManFlagNonXmlText</b> for 
    use in the <i>flags</i> parameter of the 
    <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession::Enumerate</a> method.

<b>WSManFlagNonXmlText</b> is a constant in the 
    <b>__WSManEnumFlags</b> enumeration. For more information, see 
    <a href="/windows/desktop/WinRM/enumeration-constants">Enumeration Constants</a>.

## -parameters

### -param flags [out]

The value of the constant.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>