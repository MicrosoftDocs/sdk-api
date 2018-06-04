---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IServiceTransactionConfigBase::BringYourOwnTransaction


## -description


Enables you to run the enclosed code in an existing transaction that you provide.


## -parameters




### -param szTipURL [in]

The Transaction Internet Protocol (TIP) URL of the existing transaction in which you want to run the enclosed code.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



When you bring your own transaction, that transaction's settings override the settings from the inherited methods of the <a href="https://msdn.microsoft.com/e4740bf4-51b1-474f-9637-7c5d78f0def5">IServiceTransactionConfigBase</a> interface.

The <a href="https://msdn.microsoft.com/be4fa727-962e-4254-8615-58f6ced15fc3">IServiceTransactionConfig::ConfigureBYOT</a> and the <b>BringYourOwnTransaction</b> methods are identical in behavior; the only difference is the type of parameter passed to each method.




## -see-also




<a href="https://msdn.microsoft.com/492875cb-52a7-484f-810e-bd838373b603">Bring Your Own Transaction (BYOT)</a>



<a href="https://msdn.microsoft.com/e4740bf4-51b1-474f-9637-7c5d78f0def5">IServiceTransactionConfigBase</a>
 

 

