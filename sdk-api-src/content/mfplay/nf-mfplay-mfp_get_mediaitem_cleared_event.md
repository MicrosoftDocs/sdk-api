---
UID: NF:mfplay.MFP_GET_MEDIAITEM_CLEARED_EVENT
title: MFP_GET_MEDIAITEM_CLEARED_EVENT macro (mfplay.h)
author: windows-sdk-content
description: Casts an MFP_EVENT_HEADER pointer to an MEDIAITEM_CLEARED_EVENT pointer.
old-location: mf\mfp_get_mediaitem_cleared_event.htm
tech.root: medfound
ms.assetid: 1e3c0882-2a8a-4fe9-9f05-5a343acea456
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFP_GET_MEDIAITEM_CLEARED_EVENT, MFP_GET_MEDIAITEM_CLEARED_EVENT macro [Media Foundation], mf.mfp_get_mediaitem_cleared_event, mfplay/MFP_GET_MEDIAITEM_CLEARED_EVENT
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfplay.h
api_name:
 - MFP_GET_MEDIAITEM_CLEARED_EVENT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFP_GET_MEDIAITEM_CLEARED_EVENT macro


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Casts an <a href="https://msdn.microsoft.com/ed9d3790-845a-4392-b755-6a5ce6e20de5">MFP_EVENT_HEADER</a> pointer to an <a href="https://msdn.microsoft.com/74218ab7-75a7-49e6-bfaa-5f57b1788a19">MEDIAITEM_CLEARED_EVENT</a> pointer.


## -parameters




### -param pHdr

Pointer to an <a href="https://msdn.microsoft.com/ed9d3790-845a-4392-b755-6a5ce6e20de5">MFP_EVENT_HEADER</a> structure.


## -remarks



The <b>eEventType</b> member of the input structure must be <b>MFP_EVENT_TYPE_MEDIAITEM_CLEARED</b>. Otherwise, the macro returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/c460b1cd-13d7-4b65-a755-23b2ea87864d">Media Foundation Macros</a>
 

 

