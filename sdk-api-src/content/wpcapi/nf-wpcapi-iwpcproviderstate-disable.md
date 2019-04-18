---
UID: NF:wpcapi.IWPCProviderState.Disable
title: IWPCProviderState::Disable (wpcapi.h)
author: windows-sdk-content
description: Notifies the third-party application that it is not the current provider.
old-location: parcon\iwpcproviderstate_disable.htm
tech.root: parcon
ms.assetid: 2aa1a236-b681-4226-a337-507d0854955d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Disable, Disable method, Disable method,IWPCProviderState interface, IWPCProviderState interface,Disable method, IWPCProviderState.Disable, IWPCProviderState::Disable, parcon.iwpcproviderstate_disable, wpcapi/IWPCProviderState::Disable
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
 - IWPCProviderState.Disable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWPCProviderState::Disable


## -description


Notifies the third-party application that it is not the current provider.


## -parameters






## -returns



If the method succeeds, the function returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This method is called for every registered provider when the current provider changes. This means that the <b>Disable</b> method may be called for a provider that has already been disabled.




## -see-also




<a href="https://msdn.microsoft.com/a5cd14df-8e64-4f34-801c-9901c7d215f9">IWPCProviderState</a>
 

 

