---
UID: NF:wbemdisp.ISWbemObjectSet.Item
title: ISWbemObjectSet::Item
author: windows-sdk-content
description: The Item method of the SWbemObjectSet object gets an SWbemObject from the collection.
old-location: wmi\swbemobjectset_item.htm
old-project: WmiSdk
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISWbemObjectSet interface [Windows Management Instrumentation],Item method, ISWbemObjectSet.Item, ISWbemObjectSet::Item, Item, Item method [Windows Management Instrumentation], Item method [Windows Management Instrumentation],ISWbemObjectSet interface, Item method [Windows Management Instrumentation],SWbemObjectSet object, SWbemObjectSet object [Windows Management Instrumentation],Item method, SWbemObjectSet.Item, _hmm_swbemobjectset.item, wmi.swbemobjectset_item
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
 - SWbemObjectSet.Item
 - ISWbemObjectSet.Item
 - ISWbemObjectSet.Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObjectSet::Item


## -description


The 
<b>Item</b> method of the 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> object gets an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> from the collection.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strObjectPath

Required. Relative path of the object to retrieve from the collection. Example: Win32_LogicalDisk="C:"


### -param iFlags




### -param objWbemObject






## -returns



If successful, the requested 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object returns.




## -remarks



The 
<b>Item</b> method can require a lot of processor time because complete enumeration by the provider of the elements of the set is required to return the result.



