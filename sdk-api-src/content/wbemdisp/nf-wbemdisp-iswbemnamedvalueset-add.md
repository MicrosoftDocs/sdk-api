---
UID: NF:wbemdisp.ISWbemNamedValueSet.Add
title: ISWbemNamedValueSet::Add
author: windows-sdk-content
description: The Add method of the SWbemNamedValueSet object adds an SWbemNamedValue object to the collection. If an element already exists in the collection with the same name, the new element replaces it.
old-location: wmi\swbemnamedvalueset_add.htm
old-project: WmiSdk
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: Add, Add method [Windows Management Instrumentation], Add method [Windows Management Instrumentation],ISWbemNamedValueSet interface, Add method [Windows Management Instrumentation],SWbemNamedValueSet object, ISWbemNamedValueSet interface [Windows Management Instrumentation],Add method, ISWbemNamedValueSet.Add, ISWbemNamedValueSet::Add, SWbemNamedValueSet object [Windows Management Instrumentation],Add method, SWbemNamedValueSet.Add, _hmm_swbemnamedvalueset.add, wmi.swbemnamedvalueset_add
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
 - SWbemNamedValueSet.Add
 - ISWbemNamedValueSet.Add
 - ISWbemNamedValueSet.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemNamedValueSet::Add


## -description


The 
<b>Add</b> method of the 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object adds an 
<a href="https://msdn.microsoft.com/3f72afcd-6e10-4200-804d-918e3eb2862f">SWbemNamedValue</a> object to the collection. If an element already exists in the collection with the same name, the new element replaces it.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strName [in]

Required. Name of the new value.


### -param varValue




### -param iFlags [in, optional]

Reserved and must be set to zero if specified.


### -param objWbemNamedValue






#### - varVal [in]

Required. Variant that represents the new value.


## -returns



If successful, this method returns the newly modified or newly created 
<a href="https://msdn.microsoft.com/3f72afcd-6e10-4200-804d-918e3eb2862f">SWbemNamedValue</a> object.




## -remarks



For examples of adding and retrieving named values, see 
<a href="https://msdn.microsoft.com/f9609bd2-893a-48c3-9faa-93cd033c4109">SWbemNamedValue.Value</a>.




## -see-also




<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a>
 

 

