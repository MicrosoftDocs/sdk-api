---
UID: NF:wpcapi.IWPCProviderState.Enable
title: IWPCProviderState::Enable
author: windows-sdk-content
description: Notifies the third-party application that it has been selected as the new current provider.
old-location: parcon\iwpcproviderstate_enable.htm
tech.root: parcon
ms.assetid: 6714702d-e623-43f8-9a4e-dd1b3939d011
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Enable, Enable method, Enable method,IWPCProviderState interface, IWPCProviderState interface,Enable method, IWPCProviderState.Enable, IWPCProviderState::Enable, parcon.iwpcproviderstate_enable, wpcapi/IWPCProviderState::Enable
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IWPCProviderState::Enable


## -description


Notifies the third-party application that it has been selected as the new current provider.


## -parameters






## -returns



If the method succeeds, the function returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This method is called when the current provider is changed through the drop-down list in the Parental Controls Control Panel.




## -see-also




<a href="https://msdn.microsoft.com/a5cd14df-8e64-4f34-801c-9901c7d215f9">IWPCProviderState</a>
 

 

