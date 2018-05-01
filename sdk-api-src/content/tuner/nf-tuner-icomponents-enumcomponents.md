---
UID: NF:tuner.IComponents.EnumComponents
title: IComponents::EnumComponents method
author: windows-driver-content
description: The EnumComponents method returns an enumerator for the components in the collection.
old-location: mstv\icomponents_enumcomponents.htm
old-project: mstv
ms.assetid: 214030ff-8aec-46df-8b59-f31fe926d8aa
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: EnumComponents method [Microsoft TV Technologies], EnumComponents method [Microsoft TV Technologies], IComponents interface, EnumComponents,IComponents.EnumComponents, IComponents, IComponents interface [Microsoft TV Technologies], EnumComponents method, IComponents::EnumComponents, IComponentsEnumComponents, mstv.icomponents_enumcomponents, tuner/IComponents::EnumComponents
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IComponents.EnumComponents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponents::EnumComponents method


## -description



The <b>EnumComponents</b> method returns an enumerator for the components in the collection.




## -parameters




### -param ppNewEnum [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/8811021c-8c14-4be6-8802-76b942bb34d8">IEnumComponents</a> interface pointer.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



If the method succeeds, the <b>IEnumComponents</b> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/670b47ba-bcbd-4281-95e3-a5d784f0610b">IComponents Interface</a>
 

 

