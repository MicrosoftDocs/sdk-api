---
UID: NF:tuner.ITuningSpaces.get_EnumTuningSpaces
title: ITuningSpaces::get_EnumTuningSpaces method
author: windows-driver-content
description: The get_EnumTuningSpaces method returns an enumerator for the collection.
old-location: mstv\ituningspaces_get_enumtuningspaces.htm
old-project: mstv
ms.assetid: 0d3fb395-191c-4862-8eba-07b5502dc5d4
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ITuningSpaces, ITuningSpaces interface [Microsoft TV Technologies], get_EnumTuningSpaces method, ITuningSpaces::get_EnumTuningSpaces, ITuningSpacesget_EnumTuningSpaces, get_EnumTuningSpaces method [Microsoft TV Technologies], get_EnumTuningSpaces method [Microsoft TV Technologies], ITuningSpaces interface, get_EnumTuningSpaces,ITuningSpaces.get_EnumTuningSpaces, mstv.ituningspaces_get_enumtuningspaces, tuner/ITuningSpaces::get_EnumTuningSpaces
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
-	ITuningSpaces.get_EnumTuningSpaces
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpaces::get_EnumTuningSpaces method


## -description



The <b>get_EnumTuningSpaces</b> method returns an enumerator for the collection.




## -parameters




### -param NewEnum






#### - ppNewEnum [out]

Pointer to a variable that receives an <a href="https://msdn.microsoft.com/9b64a48f-ebab-46af-a89d-b8bc488d85da">IEnumTuningSpaces</a> interface pointer. Use this interface to iterate through the collection. The caller must release the interface.


## -returns



Returns S_OK if successful.




## -see-also




<a href="https://msdn.microsoft.com/db252e22-8efe-4bfc-8fd3-2be7022bbbbd">ITuningSpaces Interface</a>
 

 

