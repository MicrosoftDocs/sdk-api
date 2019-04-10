---
UID: NF:tuner.IDVBTLocator.get_LPInnerFEC
title: IDVBTLocator::get_LPInnerFEC (tuner.h)
author: windows-sdk-content
description: The get_LPInnerFEC method retrieves the inner FEC type of the low-priority stream.
old-location: mstv\idvbtlocator_get_lpinnerfec.htm
tech.root: mstv
ms.assetid: 069904ad-5faa-4ac4-bf30-538284de2de8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],get_LPInnerFEC method, IDVBTLocator.get_LPInnerFEC, IDVBTLocator::get_LPInnerFEC, IDVBTLocatorget_LPInnerFEC, get_LPInnerFEC, get_LPInnerFEC method [Microsoft TV Technologies], get_LPInnerFEC method [Microsoft TV Technologies],IDVBTLocator interface, mstv.idvbtlocator_get_lpinnerfec, tuner/IDVBTLocator::get_LPInnerFEC
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IDVBTLocator.get_LPInnerFEC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVBTLocator::get_LPInnerFEC


## -description



The <b>get_LPInnerFEC</b> method retrieves the inner FEC type of the low-priority stream.




## -parameters




### -param FEC [out]

Receives a member of the <a href="https://msdn.microsoft.com/6910c51d-4176-49a3-be6b-6b072ad03fc1">FECMethod</a> enumeration.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/f5a95a68-fee0-404c-b9c6-6b808977f8d2">IDVBTLocator Interface</a>
 

 

