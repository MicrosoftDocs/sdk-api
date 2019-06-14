---
UID: NF:wpcapi.IWPCProviderState.Enable
title: IWPCProviderState::Enable (wpcapi.h)
author: windows-sdk-content
description: Notifies the third-party application that it has been selected as the new current provider.
old-location: parcon\iwpcproviderstate_enable.htm
tech.root: parcon
ms.assetid: 6714702d-e623-43f8-9a4e-dd1b3939d011
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Enable, Enable method, Enable method,IWPCProviderState interface, IWPCProviderState interface,Enable method, IWPCProviderState.Enable, IWPCProviderState::Enable, parcon.iwpcproviderstate_enable, wpcapi/IWPCProviderState::Enable
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCProviderState.Enable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWPCProviderState::Enable


## -description


Notifies the third-party application that it has been selected as the new current provider.


## -parameters






## -returns



If the method succeeds, the function returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



This method is called when the current provider is changed through the drop-down list in the Parental Controls Control Panel.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wpcapi/nn-wpcapi-iwpcproviderstate">IWPCProviderState</a>
 

 

