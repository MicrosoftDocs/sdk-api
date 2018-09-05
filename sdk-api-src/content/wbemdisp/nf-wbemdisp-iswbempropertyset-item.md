---
UID: NF:wbemdisp.ISWbemPropertySet.Item
title: ISWbemPropertySet::Item
author: windows-sdk-content
description: The Item method of the SWbemPropertySet object gets a named SWbemProperty from the collection. This is the default method for this object.
old-location: wmi\swbempropertyset_item.htm
old-project: WmiSdk
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: ISWbemPropertySet interface [Windows Management Instrumentation],Item method, ISWbemPropertySet.Item, ISWbemPropertySet::Item, Item, Item method [Windows Management Instrumentation], Item method [Windows Management Instrumentation],ISWbemPropertySet interface, Item method [Windows Management Instrumentation],SWbemPropertySet object, SWbemPropertySet object [Windows Management Instrumentation],Item method, SWbemPropertySet.Item, _hmm_swbempropertyset.item, wmi.swbempropertyset_item
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
 - SWbemPropertySet.Item
 - ISWbemPropertySet.Item
 - ISWbemPropertySet.Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemPropertySet::Item


## -description


The 
<b>Item</b> method of the 
<a href="https://msdn.microsoft.com/0edad17b-facc-4885-9ce4-561ca6f57a66">SWbemPropertySet</a> object gets a named 
<a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a> from the collection. This is the default method for this object.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strName [in]

Required. Name of the property to retrieve.


### -param iFlags [in, optional]

Reserved. This value must be zero if specified.


### -param objWbemProperty






## -returns



If successful, the requested 
<a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a> object is returned.



