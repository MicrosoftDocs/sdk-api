---
UID: NF:comsvcs.IProcessInitializer.Startup
title: IProcessInitializer::Startup
author: windows-sdk-content
description: Called when Dllhost.exe starts.
old-location: cos\iprocessinitializer_startup.htm
old-project: cossdk
ms.assetid: 0ba8844e-a1ef-4a1a-aef6-abd828ec59b0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IProcessInitializer interface [COM+],Startup method, IProcessInitializer.Startup, IProcessInitializer::Startup, Startup, Startup method [COM+], Startup method [COM+],IProcessInitializer interface, _cos_IProcessInitializer_Startup, comsvcs/IProcessInitializer::Startup, cos.iprocessinitializer_startup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IProcessInitializer.Startup
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IProcessInitializer::Startup


## -description


Called when Dllhost.exe starts.



## -parameters




### -param punkProcessControl [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the COM component starting up.

<b>Windows XP/2000:  </b>This parameter is always <b>NULL</b>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface referenced by <i>punkProcessControl</i> must belong to a COM component that implements an <a href="https://msdn.microsoft.com/acce67ef-3290-4892-b56a-77a256776c80">IProcessInitControl</a> interface; this interface supports the single method <a href="https://msdn.microsoft.com/1045b9c9-d7ad-4306-bd9d-7c2a4bda9a62">ResetInitializerTimeout</a>. The initialization code in <b>Startup</b> can call the <b>ResetInitializerTimeout</b> method, with <i>dwSecondsRemaining</i> set equal to the number of seconds remaining before the startup of the component times out.





## -see-also




<a href="https://msdn.microsoft.com/7c7edeb7-5bc1-4ede-8fe4-78fc7c6bdd30">IProcessInitializer</a>
 

 

