---
UID: NF:wbemdisp.ISWbemRefresher.AddEnum
title: ISWbemRefresher::AddEnum
author: windows-sdk-content
description: Adds a new enumerator to the SWbemRefresher object. This enumerator is for all the instances of the class that is specified in the strClass parameter.
old-location: wmi\swbemrefresher_addenum.htm
old-project: WmiSdk
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: AddEnum, AddEnum method [Windows Management Instrumentation], AddEnum method [Windows Management Instrumentation],ISWbemRefresher interface, AddEnum method [Windows Management Instrumentation],SWbemRefresher object, ISWbemRefresher interface [Windows Management Instrumentation],AddEnum method, ISWbemRefresher.AddEnum, ISWbemRefresher::AddEnum, SWbemRefresher object [Windows Management Instrumentation],AddEnum method, SWbemRefresher.AddEnum, _hmm_swbemrefresher.addenum, wmi.swbemrefresher_addenum
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
 - SWbemRefresher.AddEnum
 - ISWbemRefresher.AddEnum
 - ISWbemRefresher.AddEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemRefresher::AddEnum


## -description


The <b>SWbemRefresher.AddEnum</b> method adds a new enumerator to the 
<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a> object. This enumerator is for all the instances of the class that is specified in the <i>strClass</i> parameter.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemServices




### -param bsClassName




### -param iFlags [optional]

String that contains the object path of the object for which the method is executed.


### -param objWbemNamedValueSet




### -param objWbemRefreshableItem






#### - objWbemService

Required. An 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object that represents a connection to the namespace in which the object that is being added to the refresher resides.


#### - strClass

Required. String that contains the class that is being added to the refresher. This class is used as an enumerator of the instances of the class. The 
<a href="https://msdn.microsoft.com/f076eb01-1e71-487d-a1af-687a052b4d67">Index</a> property of the returned 
<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a> represents the index of the enumerator in the refresher collection.


#### - objWbemNamedvalueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that  services the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



If the call is successful, an 
<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a> object that contains an enumerator for all the instances for the specified class is returned.




## -see-also




<a href="https://msdn.microsoft.com/cc5872a1-932b-4b68-9f5e-a91d35c8e117">SWbemRefresher</a>
 

 

