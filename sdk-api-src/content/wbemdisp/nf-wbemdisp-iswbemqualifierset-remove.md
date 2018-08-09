---
UID: NF:wbemdisp.ISWbemQualifierSet.Remove
title: ISWbemQualifierSet::Remove
author: windows-sdk-content
description: The Remove method of the SWbemQualifierSet object deletes a named qualifier from the collection.
old-location: wmi\swbemqualifierset_remove.htm
old-project: WmiSdk
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemQualifierSet interface [Windows Management Instrumentation],Remove method, ISWbemQualifierSet.Remove, ISWbemQualifierSet::Remove, Remove, Remove method [Windows Management Instrumentation], Remove method [Windows Management Instrumentation],ISWbemQualifierSet interface, Remove method [Windows Management Instrumentation],SWbemQualifierSet object, SWbemQualifierSet object [Windows Management Instrumentation],Remove method, SWbemQualifierSet.Remove, _hmm_swbemqualifierset.remove, wmi.swbemqualifierset_remove
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
 - SWbemQualifierSet.Remove
 - ISWbemQualifierSet.Remove
 - ISWbemQualifierSet.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemQualifierSet::Remove


## -description


The 
<b>Remove</b> method of the 
<a href="https://msdn.microsoft.com/7ac5469c-357b-499d-a558-30bf760c5311">SWbemQualifierSet</a> object deletes a named qualifier from the collection.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strName [in]

Required. Name of the qualifier to remove.


### -param iFlags [in, optional]

Reserved. The default value is 0.


## -returns



This method does not return a value.




## -remarks



You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element. For more information, see 
<a href="https://msdn.microsoft.com/c1ebe529-33cb-4158-923d-124d6328fc60">Accessing a Collection</a>.




## -see-also




<a href="https://msdn.microsoft.com/7ac5469c-357b-499d-a558-30bf760c5311">SWbemQualifierSet</a>



<a href="https://msdn.microsoft.com/8f4c4da2-4890-4515-a3dc-76d154dae43c">SWbemQualifierSet.Add</a>
 

 

