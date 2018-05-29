---
UID: NF:tuner.IComponents.Add
title: IComponents::Add
author: windows-sdk-content
description: The Add method adds a Component object to the collection.
old-location: mstv\icomponents_add.htm
old-project: mstv
ms.assetid: ec5d9d6c-4957-46f2-9798-6e30c934459e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Add, Add method [Microsoft TV Technologies], Add method [Microsoft TV Technologies],IComponents interface, IComponents interface [Microsoft TV Technologies],Add method, IComponents.Add, IComponents::Add, IComponentsAdd, mstv.icomponents_add, tuner/IComponents::Add
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IComponents.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponents::Add


## -description



The <b>Add</b> method adds a <b>Component</b> object to the collection.




## -parameters




### -param Component




### -param NewIndex






#### - pComponent [in]

Pointer to the <b>Component</b> object to be added.


#### - pNewIndex [out]

Pointer to a <b>VARIANT</b> that will receive the index of the <b>Component</b> object after it has been added.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/670b47ba-bcbd-4281-95e3-a5d784f0610b">IComponents Interface</a>
 

 

