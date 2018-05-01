---
UID: NF:tuner.ITuningSpaces.get__NewEnum
title: ITuningSpaces::get__NewEnum method
author: windows-driver-content
description: The get__NewEnum method returns an enumerator for the collection.
old-location: mstv\ituningspaces_get__newenum.htm
old-project: mstv
ms.assetid: 9f0aec7a-954d-4399-8d15-5869c5353677
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ITuningSpaces, ITuningSpaces interface [Microsoft TV Technologies], get__NewEnum method, ITuningSpaces::get__NewEnum, ITuningSpacesget__NewEnum, get__NewEnum method [Microsoft TV Technologies], get__NewEnum method [Microsoft TV Technologies], ITuningSpaces interface, get__NewEnum,ITuningSpaces.get__NewEnum, mstv.ituningspaces_get__newenum, tuner/ITuningSpaces::get__NewEnum
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
-	ITuningSpaces.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpaces::get__NewEnum method


## -description



The <b>get__NewEnum</b> method returns an enumerator for the collection.



This method is provided to enable scripting and Visual Basic applications to iterate through the collection in a <code>For...Each</code> loop. C++ applications should use the <a href="https://msdn.microsoft.com/0d3fb395-191c-4862-8eba-07b5502dc5d4">ITuningSpaces::get_EnumTuningSpaces</a> method.


## -parameters




### -param NewEnum






#### - ppNewEnum [out]

Pointer to a variable that receives an <b>IEnumVARIANT</b> interface pointer. The caller must release the interface.


## -returns



Returns S_OK if successful.




## -remarks



The returned <b>IEnumVARIANT</b> interface is not thread safe, because it is intended primarily for use by Automation clients. Clients should not call methods on the interface from more than one thread.




## -see-also




<a href="https://msdn.microsoft.com/db252e22-8efe-4bfc-8fd3-2be7022bbbbd">ITuningSpaces Interface</a>
 

 

