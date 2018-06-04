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

# ITuningSpace::get_DefaultPreferredComponentTypes


## -description



The <b>get_DefaultPreferredComponentTypes</b> method returns an list of the default preferred component types for this tuning space.




## -parameters




### -param ComponentTypes






#### - ppComponentTypes [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/47c3837b-1348-4359-ad3d-3d82c5fe3781">IComponentTypes</a> interface pointer. Use this interface to enumerate the component types. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



A component is a stream within the program. An example of a preferred component type would be an audio stream in English. When multiple components are available, the Tuner attempts to play the preferred ones first.

If the tuning space does not have any default preferred types, this method succeeds but returns the value <b>NULL</b> in the <i>ppComponentTypes</i> parameter. Check for a <b>NULL</b> value before attempting to dereference the pointer.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

