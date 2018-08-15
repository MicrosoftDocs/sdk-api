---
UID: NF:tuner.IDVBSLocator.get_WestPosition
title: IDVBSLocator::get_WestPosition
author: windows-sdk-content
description: The get_WestPosition method retrieves a value indicating whether the orbital position is given in east or west longitude.
old-location: mstv\idvbslocator_get_westposition.htm
old-project: mstv
ms.assetid: 97bb32ba-02ca-4ea4-8364-6edddbb05d8c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],get_WestPosition method, IDVBSLocator.get_WestPosition, IDVBSLocator::get_WestPosition, IDVBSLocatorget_WestPosition, get_WestPosition, get_WestPosition method [Microsoft TV Technologies], get_WestPosition method [Microsoft TV Technologies],IDVBSLocator interface, mstv.idvbslocator_get_westposition, tuner/IDVBSLocator::get_WestPosition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.redist: 
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
 - IDVBSLocator.get_WestPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBSLocator::get_WestPosition


## -description



The <b>get_WestPosition</b> method retrieves a value indicating whether the orbital position is given in east or west longitude.




## -parameters




### -param WestLongitude






#### - pWestLongitude [out]

Pointer to a variable of type <b>VARIANT_BOOL</b>; a value of true means "west longitude."


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/a9f02e78-3800-4b14-81df-acab01ea072b">IDVBSLocator Interface</a>
 

 

