---
UID: NF:tuner.IComponents.Clone
title: IComponents::Clone
author: windows-sdk-content
description: The Clone method creates a new copy of the collection.
old-location: mstv\icomponents_clone.htm
tech.root: MSTV
ms.assetid: 5a98e265-8bef-4978-a257-1519006e9124
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IComponents interface, IComponents interface [Microsoft TV Technologies],Clone method, IComponents.Clone, IComponents::Clone, IComponentsClone, mstv.icomponents_clone, tuner/IComponents::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IComponents.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tuner.h
: 
- IComponents.Clone
: 
---

# IComponents::Clone


## -description



The <b>Clone</b> method creates a new copy of the collection.




## -parameters




### -param NewList

TBD




#### - ppNewList [out]

Address of an <a href="https://msdn.microsoft.com/670b47ba-bcbd-4281-95e3-a5d784f0610b">IComponents</a> interface pointer that will be set to the new <b>Components</b> object.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/670b47ba-bcbd-4281-95e3-a5d784f0610b">IComponents Interface</a>
 

 

