---
UID: NF:wbemdisp.ISWbemQualifierSet.Item
title: ISWbemQualifierSet::Item
author: windows-sdk-content
description: The Item method of the SWbemQualifierSet object returns a named SWbemQualifier object from the collection. This is the default method of this object.
old-location: wmi\swbemqualifierset_item.htm
old-project: WmiSdk
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: ISWbemQualifierSet interface [Windows Management Instrumentation],Item method, ISWbemQualifierSet.Item, ISWbemQualifierSet::Item, Item, Item method [Windows Management Instrumentation], Item method [Windows Management Instrumentation],ISWbemQualifierSet interface, Item method [Windows Management Instrumentation],SWbemQualifierSet object, SWbemQualifierSet object [Windows Management Instrumentation],Item method, SWbemQualifierSet.Item, _hmm_swbemqualifierset.item, wmi.swbemqualifierset_item
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
 - SWbemQualifierSet.Item
 - ISWbemQualifierSet.Item
 - ISWbemQualifierSet.Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemQualifierSet::Item


## -description


The 
<b>Item</b> method of the 
<a href="https://msdn.microsoft.com/7ac5469c-357b-499d-a558-30bf760c5311">SWbemQualifierSet</a> object returns a named 
<a href="https://msdn.microsoft.com/b5dbe98a-e1d8-4679-a563-c88760d08b79">SWbemQualifier</a> object from the collection. This is the default method of this object.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param name




### -param iFlags [in, optional]

Reserved. The default value is 0 (zero).


### -param objWbemQualifier






#### - strName [in]

Required. Name of the qualifier to retrieve.


## -returns



If successful, the requested 
<a href="https://msdn.microsoft.com/b5dbe98a-e1d8-4679-a563-c88760d08b79">SWbemQualifier</a> object is returned.




## -see-also




<a href="https://msdn.microsoft.com/b5dbe98a-e1d8-4679-a563-c88760d08b79">SWbemQualifier</a>



<a href="https://msdn.microsoft.com/7ac5469c-357b-499d-a558-30bf760c5311">SWbemQualifierSet</a>
 

 

