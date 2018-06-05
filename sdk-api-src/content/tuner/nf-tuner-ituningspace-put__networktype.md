---
UID: NF:tuner.ITuningSpace.put__NetworkType
title: ITuningSpace::put__NetworkType
author: windows-sdk-content
description: The put_NetworkType method specifies the network type of the tuning space.
old-location: mstv\ituningspace_put__networktype.htm
old-project: mstv
ms.assetid: 02e4ec53-e527-4cd2-a424-66c2f3fe4e43
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],put__NetworkType method, ITuningSpace.put__NetworkType, ITuningSpace::put__NetworkType, ITuningSpaceput__NetworkType, mstv.ituningspace_put__networktype, put__NetworkType, put__NetworkType method [Microsoft TV Technologies], put__NetworkType method [Microsoft TV Technologies],ITuningSpace interface, tuner/ITuningSpace::put__NetworkType
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	ITuningSpace.put__NetworkType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::put__NetworkType


## -description



The <b>put_NetworkType</b> method specifies the network type of the tuning space.




## -parameters




### -param NetworkTypeGuid [in]

Specifies the network type GUID. This GUID corresponds to the CLSID of the Network Provider for the tuning space. The value GUID_NULL means the tuning space does not use a Network Provider filter.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

