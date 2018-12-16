---
UID: NF:tuner.IComponents.get_Count
title: IComponents::get_Count
author: windows-sdk-content
description: The get_Count method gets the number of Component objects in the collection.
old-location: mstv\icomponents_get_count.htm
tech.root: mstv
ms.assetid: ba198e27-c699-4c93-aa2d-b8be8c40380c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComponents interface [Microsoft TV Technologies],get_Count method, IComponents.get_Count, IComponents::get_Count, IComponentsget_Count, get_Count, get_Count method [Microsoft TV Technologies], get_Count method [Microsoft TV Technologies],IComponents interface, mstv.icomponents_get_count, tuner/IComponents::get_Count
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponents.get_Count
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponents::get_Count


## -description



The <b>get_Count</b> method gets the number of <b>Component</b> objects in the collection.




## -parameters




### -param Count [out]

Pointer to a variable of type <b>long</b> that receives the number of components.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/670b47ba-bcbd-4281-95e3-a5d784f0610b">IComponents Interface</a>
 

 

