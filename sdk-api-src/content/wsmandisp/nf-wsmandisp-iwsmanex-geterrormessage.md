---
UID: NF:wsmandisp.IWSManEx.GetErrorMessage
title: IWSManEx::GetErrorMessage (wsmandisp.h)
description: Returns a formatted string containing the text of an error number.
helpviewer_keywords: ["GetErrorMessage","GetErrorMessage method [Windows Remote Management]","GetErrorMessage method [Windows Remote Management]","IWSManEx interface","IWSManEx interface [Windows Remote Management]","GetErrorMessage method","IWSManEx.GetErrorMessage","IWSManEx::GetErrorMessage","winrm.iwsmanex_geterrormessage","wsmandisp/IWSManEx::GetErrorMessage"]
old-location: winrm\iwsmanex_geterrormessage.htm
tech.root: winrm
ms.assetid: af5ae515-458a-4d7f-80f8-0fd51f97e7f1
ms.date: 12/05/2018
ms.keywords: GetErrorMessage, GetErrorMessage method [Windows Remote Management], GetErrorMessage method [Windows Remote Management],IWSManEx interface, IWSManEx interface [Windows Remote Management],GetErrorMessage method, IWSManEx.GetErrorMessage, IWSManEx::GetErrorMessage, winrm.iwsmanex_geterrormessage, wsmandisp/IWSManEx::GetErrorMessage
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
 - IWSManEx::GetErrorMessage
 - wsmandisp/IWSManEx::GetErrorMessage
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
 - IWSManEx.GetErrorMessage
---

# IWSManEx::GetErrorMessage


## -description

Returns a formatted string containing the text of an error number. This method performs the same operation as the <b>Winrm</b> command-line <b>winrm helpmsg </b><i>error number</i>.

## -parameters

### -param errorNumber [in]

Error message number in decimal or hexadecimal from WinRM, WinHTTP, or other operating system components.

### -param errorMessage [out]

Error message string formatted like messages returned from the  <b>Winrm</b> command.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The corresponding scripting method is <a href="/windows/desktop/WinRM/wsman-geterrormessage">WSMan.GetErrorMessage</a>.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanex">IWSManEx</a>



<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>