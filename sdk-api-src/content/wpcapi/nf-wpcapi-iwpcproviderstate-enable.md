---
UID: NF:wpcapi.IWPCProviderState.Enable
title: IWPCProviderState::Enable (wpcapi.h)
description: Notifies the third-party application that it has been selected as the new current provider.
helpviewer_keywords: ["Enable","Enable method","Enable method","IWPCProviderState interface","IWPCProviderState interface","Enable method","IWPCProviderState.Enable","IWPCProviderState::Enable","parcon.iwpcproviderstate_enable","wpcapi/IWPCProviderState::Enable"]
old-location: parcon\iwpcproviderstate_enable.htm
tech.root: parcon
ms.assetid: 6714702d-e623-43f8-9a4e-dd1b3939d011
ms.date: 12/05/2018
ms.keywords: Enable, Enable method, Enable method,IWPCProviderState interface, IWPCProviderState interface,Enable method, IWPCProviderState.Enable, IWPCProviderState::Enable, parcon.iwpcproviderstate_enable, wpcapi/IWPCProviderState::Enable
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wpcprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWPCProviderState::Enable
 - wpcapi/IWPCProviderState::Enable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCProviderState.Enable
---

# IWPCProviderState::Enable


## -description

Notifies the third-party application that it has been selected as the new current provider.



## -returns

If the method succeeds, the function returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This method is called when the current provider is changed through the drop-down list in the Parental Controls Control Panel.

## -see-also

<a href="/windows/desktop/api/wpcapi/nn-wpcapi-iwpcproviderstate">IWPCProviderState</a>
