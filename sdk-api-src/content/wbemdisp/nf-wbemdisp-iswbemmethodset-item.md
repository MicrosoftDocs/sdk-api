---
UID: NF:wbemdisp.ISWbemMethodSet.Item
title: ISWbemMethodSet::Item
author: windows-sdk-content
description: The Item method of the SWbemMethodSet object returns a named SWbemMethod object from the collection.
old-location: wmi\swbemmethodset_item.htm
old-project: WmiSdk
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: ISWbemMethodSet interface [Windows Management Instrumentation],Item method, ISWbemMethodSet.Item, ISWbemMethodSet::Item, Item, Item method [Windows Management Instrumentation], Item method [Windows Management Instrumentation],ISWbemMethodSet interface, Item method [Windows Management Instrumentation],SWbemMethodSet object, SWbemMethodSet object [Windows Management Instrumentation],Item method, SWbemMethodSet.Item, _hmm_swbemmethodset.item, wmi.swbemmethodset_item
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
 - SWbemMethodSet.Item
 - ISWbemMethodSet.Item
 - ISWbemMethodSet.Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemMethodSet::Item


## -description


The 
<b>Item</b> method of the 
<a href="https://msdn.microsoft.com/0ca2601f-ed40-472e-b4f2-eee750c8c8d1">SWbemMethodSet</a> object returns a named 
<a href="https://msdn.microsoft.com/461d5c41-4930-40cf-96e2-bc8cae335b60">SWbemMethod</a> object from the collection.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strName [in]

Required. Name of the method to retrieve.


### -param iFlags [in, optional]

Reserved. The default value is 0.


### -param objWbemMethod






## -returns



If successful, the requested 
<a href="https://msdn.microsoft.com/461d5c41-4930-40cf-96e2-bc8cae335b60">SWbemMethod</a> object returns.




## -see-also




<a href="https://msdn.microsoft.com/461d5c41-4930-40cf-96e2-bc8cae335b60">SWbemMethod</a>



<a href="https://msdn.microsoft.com/0ca2601f-ed40-472e-b4f2-eee750c8c8d1">SWbemMethodSet</a>
 

 

