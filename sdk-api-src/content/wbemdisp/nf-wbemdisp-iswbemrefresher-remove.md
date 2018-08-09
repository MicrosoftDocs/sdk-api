---
UID: NF:wbemdisp.ISWbemRefresher.Remove
title: ISWbemRefresher::Remove
author: windows-sdk-content
description: The SWbemRefresher.Remove method removes the SWbemRefreshableItem object with the specified index from the refresher.
old-location: wmi\swbemrefresher_remove.htm
old-project: WmiSdk
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemRefresher interface [Windows Management Instrumentation],Remove method, ISWbemRefresher.Remove, ISWbemRefresher::Remove, Remove, Remove method [Windows Management Instrumentation], Remove method [Windows Management Instrumentation],ISWbemRefresher interface, Remove method [Windows Management Instrumentation],SWbemRefresher object, SWbemRefresher object [Windows Management Instrumentation],Remove method, SWbemRefresher.Remove, _hmm_swbemrefresher.remove, wmi.swbemrefresher_remove
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemRefresher.Remove
 - ISWbemRefresher.Remove
 - ISWbemRefresher.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemRefresher::Remove


## -description



The <b>SWbemRefresher.Remove</b> method removes the 
<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a> object with the specified index from the refresher. The <b>SWbemRefreshableItem</b> object can represent either a single object or an object set.



For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iIndex




### -param iFlags [optional]

Flags must be set t0 (zero).


#### - LIndex

Index of the item in the <a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a> object.


#### - objWbemNamedvalueSet [optional]

Null.


## -returns



This method has no return values.




## -remarks



<b>Error codes</b>—If the refresher has no item with the specified index, <b>wbemErrNotFound</b> is generated.




## -see-also




<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a>
 

 

