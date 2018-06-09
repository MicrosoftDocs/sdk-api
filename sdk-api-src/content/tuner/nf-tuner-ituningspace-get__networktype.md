---
UID: NF:tuner.ITuningSpace.get__NetworkType
title: ITuningSpace::get__NetworkType
author: windows-sdk-content
description: The get_NetworkType method retrieves the network type for this tuning space.
old-location: mstv\ituningspace_get__networktype.htm
old-project: mstv
ms.assetid: 54cf0c5b-03fb-4419-976c-acc821dfc7e8
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get__NetworkType method, ITuningSpace.get__NetworkType, ITuningSpace::get__NetworkType, ITuningSpaceget__NetworkType, get__NetworkType, get__NetworkType method [Microsoft TV Technologies], get__NetworkType method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get__networktype, tuner/ITuningSpace::get__NetworkType
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
 - ITuningSpace.get__NetworkType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::get__NetworkType


## -description



The <b>get_NetworkType</b> method retrieves the network type for this tuning space.




## -parameters




### -param NetworkTypeGuid






#### - pNetworkTypeGuid [out]

Pointer to a variable that receives the network type GUID. This GUID corresponds to the CLSID of the Network Provider for the tuning space. For some tuning spaces, the network type is GUID_NULL, which means the tuning space does not use a Network Provider filter.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

