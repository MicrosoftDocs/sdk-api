---
UID: NF:tuner.ITuningSpaceContainer.get_MaxCount
title: ITuningSpaceContainer::get_MaxCount method
author: windows-driver-content
description: The get_MaxCount method retrieves the maximum number of tuning spaces allowed on the system.
old-location: mstv\ituningspacecontainer_get_maxcount.htm
old-project: mstv
ms.assetid: 72692bc6-a210-4e60-9c04-14a7ea531cb4
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITuningSpaceContainer, ITuningSpaceContainer interface [Microsoft TV Technologies], get_MaxCount method, ITuningSpaceContainer::get_MaxCount, ITuningSpaceContainerget_MaxCount, get_MaxCount method [Microsoft TV Technologies], get_MaxCount method [Microsoft TV Technologies], ITuningSpaceContainer interface, get_MaxCount,ITuningSpaceContainer.get_MaxCount, mstv.ituningspacecontainer_get_maxcount, tuner/ITuningSpaceContainer::get_MaxCount
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
-	ITuningSpaceContainer.get_MaxCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpaceContainer::get_MaxCount method


## -description



The <b>get_MaxCount</b> method retrieves the maximum number of tuning spaces allowed on the system.




## -parameters




### -param MaxCount






#### - pMaxCount [out]

Pointer to a variable that receives the maximum number of tuning spaces.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer Interface</a>
 

 

