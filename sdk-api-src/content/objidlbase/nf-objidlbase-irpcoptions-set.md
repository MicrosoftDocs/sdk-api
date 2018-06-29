---
UID: NF:objidlbase.IRpcOptions.Set
title: IRpcOptions::Set
author: windows-sdk-content
description: Sets the value of an RPC binding option property.
old-location: com\irpcoptions_set.htm
old-project: com
ms.assetid: b4412e45-adc7-47e4-a19c-9ada6407e6dc
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: IRpcOptions interface [COM],Set method, IRpcOptions.Set, IRpcOptions::Set, Set, Set method [COM], Set method [COM],IRpcOptions interface, _com_irpcoptions_set, com.irpcoptions_set, objidlbase/IRpcOptions::Set
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IRpcOptions.Set
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IRpcOptions::Set


## -description


Sets the value of an RPC binding option property.


## -parameters




### -param pPrx [in]

A pointer to the proxy whose property is being set.


### -param dwProperty [in]

An identifier of the property to be set, which must be COMBND_RPCTIMEOUT.


### -param dwValue [in]

The new value of the property.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



See <a href="https://msdn.microsoft.com/aa5db8ac-4c29-43cf-a7ed-a870df9dfb82">IRpcOptions</a> for a table of the possible values of the COMBND_RPCTIMEOUT property.




## -see-also




<a href="https://msdn.microsoft.com/aa5db8ac-4c29-43cf-a7ed-a870df9dfb82">IRpcOptions</a>
 

 

