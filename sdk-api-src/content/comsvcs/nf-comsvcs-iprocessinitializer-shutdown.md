---
UID: NF:comsvcs.IProcessInitializer.Shutdown
title: IProcessInitializer::Shutdown method
author: windows-driver-content
description: Called when Dllhost.exe shuts down.
old-location: cos\iprocessinitializer_shutdown.htm
old-project: cossdk
ms.assetid: e525ded0-971d-4711-b078-b2e6b28c313f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IProcessInitializer, IProcessInitializer interface [COM+], Shutdown method, IProcessInitializer::Shutdown, Shutdown method [COM+], Shutdown method [COM+], IProcessInitializer interface, Shutdown,IProcessInitializer.Shutdown, _cos_IProcessInitializer_Shutdown, comsvcs/IProcessInitializer::Shutdown, cos.iprocessinitializer_shutdown
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IProcessInitializer.Shutdown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IProcessInitializer::Shutdown method


## -description


Called when Dllhost.exe shuts down.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The Shutdown method is not called during a failfast or other catastrophic shutdown events.




## -see-also




<a href="https://msdn.microsoft.com/7c7edeb7-5bc1-4ede-8fe4-78fc7c6bdd30">IProcessInitializer</a>
 

 

