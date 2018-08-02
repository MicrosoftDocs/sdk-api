---
UID: NF:wbemdisp.ISWbemNamedValueSet.Item
title: ISWbemNamedValueSet::Item
author: windows-sdk-content
description: The Item method of the SWbemNamedValueSet object gets an SWbemNamedValue object from the collection.
old-location: wmi\swbemnamedvalueset_item.htm
old-project: WmiSdk
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISWbemNamedValueSet interface [Windows Management Instrumentation],Item method, ISWbemNamedValueSet.Item, ISWbemNamedValueSet::Item, Item, Item method [Windows Management Instrumentation], Item method [Windows Management Instrumentation],ISWbemNamedValueSet interface, Item method [Windows Management Instrumentation],SWbemNamedValueSet object, SWbemNamedValueSet object [Windows Management Instrumentation],Item method, SWbemNamedValueSet.Item, _hmm_swbemnamedvalueset.item, wmi.swbemnamedvalueset_item
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
 - SWbemNamedValueSet.Item
 - ISWbemNamedValueSet.Item
 - ISWbemNamedValueSet.Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemNamedValueSet::Item


## -description


The 
<b>Item</b> method of the 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object gets an 
<a href="https://msdn.microsoft.com/3f72afcd-6e10-4200-804d-918e3eb2862f">SWbemNamedValue</a> object from the collection.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strName [in]

Required. Name of the value to retrieve.


### -param iFlags [in, optional]

Reserved. This value must be zero if specified.


### -param objWbemNamedValue






## -returns



If successful, the requested 
<a href="https://msdn.microsoft.com/3f72afcd-6e10-4200-804d-918e3eb2862f">SWbemNamedValue</a> object is returned.




## -remarks



For examples of adding and retrieving named values, see 
<a href="https://msdn.microsoft.com/f9609bd2-893a-48c3-9faa-93cd033c4109">SWbemNamedValue.Value</a>.




## -see-also




<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a>
 

 

