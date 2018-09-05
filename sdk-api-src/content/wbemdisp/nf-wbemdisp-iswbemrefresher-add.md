---
UID: NF:wbemdisp.ISWbemRefresher.Add
title: ISWbemRefresher::Add
author: windows-sdk-content
description: The SWbemRefresher.Add method adds a new SWbemRefreshableItem object to the collection in the SWbemRefresher object.SWbemRefreshableItem object to the collection in the SWbemRefresher object.
old-location: wmi\swbemrefresher_add.htm
old-project: WmiSdk
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: Add, Add method [Windows Management Instrumentation], Add method [Windows Management Instrumentation],ISWbemRefresher interface, Add method [Windows Management Instrumentation],SWbemRefresher object, ISWbemRefresher interface [Windows Management Instrumentation],Add method, ISWbemRefresher.Add, ISWbemRefresher::Add, SWbemRefresher object [Windows Management Instrumentation],Add method, SWbemRefresher.Add, _hmm_swbemrefresher.add, wmi.swbemrefresher_add
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.redist: 
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
 - SWbemRefresher.Add
 - ISWbemRefresher.Add
 - ISWbemRefresher.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemRefresher::Add


## -description



The <b>SWbemRefresher.Add</b> method adds a new 
<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a> object to the collection in the 
<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a> object.



For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemServices




### -param bsInstancePath




### -param iFlags [optional]

String that contains the object path of the object for which the method is executed. 



### -param objWbemNamedValueSet




### -param objWbemRefreshableItem






#### - objWbemNamedvalueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that services the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


#### - objWbemService

Required. An 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object that represents a connection to the namespace in which the object that is being added to the refresher resides.


#### - strInstancePath

Required. String that contains the relative path of the object in the namespace. The path must contain an instance. The 
<a href="https://msdn.microsoft.com/f076eb01-1e71-487d-a1af-687a052b4d67">Index</a> property of the returned 
<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a> represents the index of the object in the refresher collection.


## -returns



If the call is successful, an 
<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a> object that  contains a single refreshable object is returned.




## -see-also




<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a>
 

 

