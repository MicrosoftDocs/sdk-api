---
UID: NF:mfplay.MFP_GET_PLAY_EVENT
title: MFP_GET_PLAY_EVENT macro
author: windows-sdk-content
description: Casts an MFP_EVENT_HEADER pointer to an MFP_PLAY_EVENT pointer.
old-location: mf\mfp_get_play_event.htm
old-project: medfound
ms.assetid: 2a67965f-3429-4ce7-ae62-8952cacb00eb
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFP_GET_PLAY_EVENT, MFP_GET_PLAY_EVENT macro [Media Foundation], mf.mfp_get_play_event, mfplay/MFP_GET_PLAY_EVENT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: "_MFP_MEDIAITEM_CHARACTERISTICS"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfplay.h
api_name:
 - MFP_GET_PLAY_EVENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MFP_GET_PLAY_EVENT macro


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Casts an <a href="https://msdn.microsoft.com/ed9d3790-845a-4392-b755-6a5ce6e20de5">MFP_EVENT_HEADER</a> pointer to an <a href="https://msdn.microsoft.com/2cf8805f-8a3c-45a6-87ad-fa4da9115833">MFP_PLAY_EVENT</a> pointer.


## -parameters




### -param pHdr

Pointer to an <a href="https://msdn.microsoft.com/ed9d3790-845a-4392-b755-6a5ce6e20de5">MFP_EVENT_HEADER</a> structure.


## -remarks



The <b>eEventType</b> member of the input structure must be <b>MFP_EVENT_TYPE_PLAY</b>. Otherwise, the macro returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/c460b1cd-13d7-4b65-a755-23b2ea87864d">Media Foundation Macros</a>
 

 

