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

# __MIDL___MIDL_itf_textstor_0000_0000_0002 enumeration


## -description


Elements of the <b>TsLayoutCode</b> enumeration are used to specify the type of layout change in an <a href="https://msdn.microsoft.com/2018d3ef-892f-46c0-8dd0-3e27a9f2272c">ITextStoreACPSink::OnLayoutChange</a> or <a href="https://msdn.microsoft.com/22629ca6-5701-4f6f-b797-bb71c8d31da6">ITextStoreAnchorSink::OnLayoutChange</a> notification.


## -enum-fields




### -field TS_LC_CREATE

The view has just been created.


### -field TS_LC_CHANGE

The view layout has changed.


### -field TS_LC_DESTROY

The view is about to be destroyed.


## -see-also




<a href="https://msdn.microsoft.com/2018d3ef-892f-46c0-8dd0-3e27a9f2272c">ITextStoreACPSink::OnLayoutChange
      </a>



<a href="https://msdn.microsoft.com/22629ca6-5701-4f6f-b797-bb71c8d31da6">
        ITextStoreAnchorSink::OnLayoutChange
      </a>
 

 

