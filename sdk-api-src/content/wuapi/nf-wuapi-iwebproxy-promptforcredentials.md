---
UID: NF:wuapi.IWebProxy.PromptForCredentials
title: IWebProxy::PromptForCredentials (wuapi.h)
description: Prompts the user for the password to use for proxy authentication.
helpviewer_keywords: ["IWebProxy interface [Windows Update Agent]","PromptForCredentials method","IWebProxy.PromptForCredentials","IWebProxy::PromptForCredentials","PromptForCredentials","PromptForCredentials method [Windows Update Agent]","PromptForCredentials method [Windows Update Agent]","IWebProxy interface","wua.iwebproxy_promptforcredentials","wuapi/IWebProxy::PromptForCredentials"]
old-location: wua\iwebproxy_promptforcredentials.htm
tech.root: wua
ms.assetid: 2eeb4418-d9fe-41b8-97c9-cafe18aab528
ms.date: 12/05/2018
ms.keywords: IWebProxy interface [Windows Update Agent],PromptForCredentials method, IWebProxy.PromptForCredentials, IWebProxy::PromptForCredentials, PromptForCredentials, PromptForCredentials method [Windows Update Agent], PromptForCredentials method [Windows Update Agent],IWebProxy interface, wua.iwebproxy_promptforcredentials, wuapi/IWebProxy::PromptForCredentials
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWebProxy::PromptForCredentials
 - wuapi/IWebProxy::PromptForCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IWebProxy.PromptForCredentials
---

# IWebProxy::PromptForCredentials


## -description

Prompts the user for the password to use for proxy authentication.

## -parameters

### -param parentWindow [in]

The parent window of the dialog box in which the user enters the credentials.

### -param title [in]

The title to use for the dialog box in which the user enters the credentials.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -remarks

This method can be changed only by a user on the computer. This method can be accessed through the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface.

If null is specified for the parent window (for example, if you specified Nothing in Visual Basic), the dialog box is displayed on the desktop.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iwebproxy">IWebProxy</a>