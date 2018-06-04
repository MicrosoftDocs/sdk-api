---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDistributorNotify::NotifyGraphChange


## -description



The <code>NotifyGraphChange</code> method is called when the set of filters in the filter graph changes or any pin connections change.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method is called whenever the <a href="https://msdn.microsoft.com/8f837917-015f-427f-b234-b0ccbcf943eb">IFilterGraph::AddFilter</a>, <a href="https://msdn.microsoft.com/ec681340-0fb9-4eba-8211-d5fa07fb076b">IFilterGraph::RemoveFilter</a>, or <a href="https://msdn.microsoft.com/fb17bd98-dd6b-4fad-9b56-9cab10725b28">IFilterGraph::ConnectDirect</a> method is called or a method is called that will lead to one of these being called (such as <a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">IGraphBuilder::RenderFile</a>).

Make sure you call <b>Release</b> on any held filters that have been removed at this point. For performance reasons, PIDs might choose not to rescan the filters until the PIDs actually need the interfaces, because there might be several separate notifications sent. However, it is important to release any cached interfaces immediately.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c7c9ee95-9d68-45c5-a3ca-8d6071782851">IDistributorNotify Interface</a>
 

 

