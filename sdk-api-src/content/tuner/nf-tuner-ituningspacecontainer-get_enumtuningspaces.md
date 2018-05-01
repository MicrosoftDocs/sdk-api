---
UID: NF:tuner.ITuningSpaceContainer.get_EnumTuningSpaces
title: ITuningSpaceContainer::get_EnumTuningSpaces method
author: windows-driver-content
description: The get_EnumTuningSpaces method retrieves a collection of all tuning spaces available on the local system.
old-location: mstv\ituningspacecontainer_get_enumtuningspaces.htm
old-project: mstv
ms.assetid: 7cd6a691-8c47-4c26-8afd-57f6965246ff
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ITuningSpaceContainer, ITuningSpaceContainer interface [Microsoft TV Technologies], get_EnumTuningSpaces method, ITuningSpaceContainer::get_EnumTuningSpaces, ITuningSpaceContainerget_EnumTuningSpaces, get_EnumTuningSpaces method [Microsoft TV Technologies], get_EnumTuningSpaces method [Microsoft TV Technologies], ITuningSpaceContainer interface, get_EnumTuningSpaces,ITuningSpaceContainer.get_EnumTuningSpaces, mstv.ituningspacecontainer_get_enumtuningspaces, tuner/ITuningSpaceContainer::get_EnumTuningSpaces
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
-	ITuningSpaceContainer.get_EnumTuningSpaces
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpaceContainer::get_EnumTuningSpaces method


## -description



The <b>get_EnumTuningSpaces</b> method retrieves a collection of all tuning spaces available on the local system.




## -parameters




### -param ppEnum [out]

Pointer to a variable that receives an <a href="https://msdn.microsoft.com/9b64a48f-ebab-46af-a89d-b8bc488d85da">IEnumTuningSpaces</a> interface pointer. Use this interface to enumerate the collection. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



C++ applications use this method to get the initial list of tuning spaces defined on the local system.




## -see-also




<a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer Interface</a>
 

 

