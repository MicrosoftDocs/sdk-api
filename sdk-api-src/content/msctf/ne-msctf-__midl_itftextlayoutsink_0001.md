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

# __MIDL_ITfTextLayoutSink_0001 enumeration


## -description


Elements of the <b>TfLayoutCode</b> enumeration specify the type of layout change in an <a href="https://msdn.microsoft.com/a99313ab-98a7-4fc0-b3ae-78ff26a41d8e">ITfTextLayoutSink::OnLayoutChange</a> notification.


## -enum-fields




### -field TF_LC_CREATE

The view has just been created.


### -field TF_LC_CHANGE

The view layout has changed.


### -field TF_LC_DESTROY

The view is about to be destroyed.


## -remarks



In TSF, a view is on-screen rendering of document content. These constants are assigned to parameters of methods of the <b>ITf*</b> interfaces, but not those of the <b>IText*</b> interfaces.




## -see-also




<a href="https://msdn.microsoft.com/a99313ab-98a7-4fc0-b3ae-78ff26a41d8e">ITfTextLayoutSink::OnLayoutChange
      </a>
 

 

