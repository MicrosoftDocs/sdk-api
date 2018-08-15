---
UID: NF:tuner.ITuner.EnumTuningSpaces
title: ITuner::EnumTuningSpaces
author: windows-sdk-content
description: The EnumTuningSpaces method creates a collection of tuning spaces preferred by this implementation.
old-location: mstv\ituner_enumtuningspaces.htm
old-project: mstv
ms.assetid: 6bd42b1b-b644-4fd7-9875-21a8d0f01243
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EnumTuningSpaces, EnumTuningSpaces method [Microsoft TV Technologies], EnumTuningSpaces method [Microsoft TV Technologies],ITuner interface, ITuner interface [Microsoft TV Technologies],EnumTuningSpaces method, ITuner.EnumTuningSpaces, ITuner::EnumTuningSpaces, ITunerEnumTuningSpaces, mstv.ituner_enumtuningspaces, tuner/ITuner::EnumTuningSpaces
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ITuner.EnumTuningSpaces
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuner::EnumTuningSpaces


## -description



The <b>EnumTuningSpaces</b> method creates a collection of tuning spaces preferred by this implementation.




## -parameters




### -param ppEnum [out]

Address of a <a href="https://msdn.microsoft.com/9b64a48f-ebab-46af-a89d-b8bc488d85da">IEnumTuningSpaces</a> interface pointer that will be set to the returned collection.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This list is a subset of the compatible tuning spaces for this implementation.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1bc965a5-6bc9-488a-a2f9-f35d0cfbcccd">ITuner Interface</a>
 

 

