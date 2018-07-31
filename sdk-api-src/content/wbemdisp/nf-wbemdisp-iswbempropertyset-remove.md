---
UID: NF:wbemdisp.ISWbemPropertySet.Remove
title: ISWbemPropertySet::Remove
author: windows-sdk-content
description: The Remove method of the SWbemPropertySet object deletes a property from the SWbemPropertySet collection.
old-location: wmi\swbempropertyset_remove.htm
old-project: WmiSdk
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISWbemPropertySet interface [Windows Management Instrumentation],Remove method, ISWbemPropertySet.Remove, ISWbemPropertySet::Remove, Remove, Remove method [Windows Management Instrumentation], Remove method [Windows Management Instrumentation],ISWbemPropertySet interface, Remove method [Windows Management Instrumentation],SWbemPropertySet object, SWbemPropertySet object [Windows Management Instrumentation],Remove method, SWbemPropertySet.Remove, _hmm_swbempropertyset.remove, wmi.swbempropertyset_remove
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
 - SWbemPropertySet.Remove
 - ISWbemPropertySet.Remove
 - ISWbemPropertySet.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemPropertySet::Remove


## -description


The 
<b>Remove</b> method of the 
<a href="https://msdn.microsoft.com/0edad17b-facc-4885-9ce4-561ca6f57a66">SWbemPropertySet</a> object deletes a property from the 
<b>SWbemPropertySet</b> collection.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strName [in]

Required. Name of the item to remove.


### -param iFlags [in, optional]

Reserved. This value must be 0 (zero) if specified.


## -returns



This method does not return a value.




## -remarks



Properties cannot be removed from class instances or derived classes with inherited properties. Such deletion attempts raise an error and the property is not removed; the property is reset to its default value.

You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element. For more information, see 
<a href="https://msdn.microsoft.com/c1ebe529-33cb-4158-923d-124d6328fc60">Accessing a Collection</a>.


#### Examples

For a code example that uses this method, see the <a href="https://msdn.microsoft.com/0edad17b-facc-4885-9ce4-561ca6f57a66">SWbemPropertySet</a> topic.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0edad17b-facc-4885-9ce4-561ca6f57a66">SWbemPropertySet</a>



<a href="https://msdn.microsoft.com/52a5f964-3d53-441b-9a58-650afdc5b1b9">SWbemPropertySet.Add</a>
 

 

