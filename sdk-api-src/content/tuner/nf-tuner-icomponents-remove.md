---
UID: NF:tuner.IComponents.Remove
title: IComponents::Remove
author: windows-sdk-content
description: The Remove method removes a Component object from the collection.
old-location: mstv\icomponents_remove.htm
old-project: mstv
ms.assetid: 0d71b1f0-1a15-4206-b22f-624cc4b246a3
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IComponents interface [Microsoft TV Technologies],Remove method, IComponents.Remove, IComponents::Remove, IComponentsRemove, Remove, Remove method [Microsoft TV Technologies], Remove method [Microsoft TV Technologies],IComponents interface, mstv.icomponents_remove, tuner/IComponents::Remove
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponents.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponents::Remove


## -description



The <b>Remove</b> method removes a <b>Component</b> object from the collection.




## -parameters




### -param Index [in]

Variable of type <b>VARIANT</b> that specifies the index number of the <b>Component</b> object to be removed.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/670b47ba-bcbd-4281-95e3-a5d784f0610b">IComponents Interface</a>
 

 

