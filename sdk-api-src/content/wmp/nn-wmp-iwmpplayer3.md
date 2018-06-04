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

# IWMPPlayer3 interface


## -description



The <b>IWMPPlayer3</b> interface provides methods for modifying the basic behavior of the control user interface. These methods supplement the <b>IWMPCore2</b> interface.



The <b>IWMPPlayer3</b> interface duplicates the methods of <b>IWMPPlayer</b> and <b>IWMPPlayer2</b> and inherits the methods of <b>IWMPCore2</b>. It is identical to <b>IWMPPlayer2</b> except for the inherited interface.

Retrieve a pointer to an <b>IWMPPlayer3</b> interface either by calling the <b>QueryInterface</b> method of the <b>IWMPPlayer</b> or <b>IWMPPlayer2</b> interface, or by calling the COM <b>CoCreateInstance</b> method.


## -see-also




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/5f839bfe-bf67-49eb-8743-57713e1be7c5">IWMPCore2 Interface</a>



<a href="https://msdn.microsoft.com/3004551e-ce36-4f15-88c3-93b2bfaa72fc">IWMPCore3 Interface</a>



<a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/bf51d54d-d0aa-42ad-8180-d1f6487baac8">IWMPPlayer2 Interface</a>



<a href="https://msdn.microsoft.com/afe5dbd1-96e1-4abe-b843-ec6130fa02d0">IWMPPlayer4 Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

