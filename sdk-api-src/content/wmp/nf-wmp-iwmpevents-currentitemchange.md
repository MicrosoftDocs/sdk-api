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

# IWMPEvents::CurrentItemChange


## -description



The <b>CurrentItemChange</b> event occurs when the user or the <b>IWMPControls::put_CurrentItem</b> method changes the current item value.




## -parameters




### -param pdispMedia [in]

Pointer to an <b>IDispatch</b> interface that identifies the new current item.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/190cec53-5cd9-4bd0-b8d9-23c5389fe231">IWMPControls::put_currentItem</a>



<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>
 

 

