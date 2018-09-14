---
UID: NF:tuner.IDVBTLocator.put_LPInnerFEC
title: IDVBTLocator::put_LPInnerFEC
author: windows-sdk-content
description: The put_LPInnerFEC method sets the inner FEC type of the low-priority stream.
old-location: mstv\idvbtlocator_put_lpinnerfec.htm
tech.root: MSTV
ms.assetid: 37b5b063-a0ae-4ef8-a63b-44c009a31eb8
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],put_LPInnerFEC method, IDVBTLocator.put_LPInnerFEC, IDVBTLocator::put_LPInnerFEC, IDVBTLocatorput_LPInnerFEC, mstv.idvbtlocator_put_lpinnerfec, put_LPInnerFEC, put_LPInnerFEC method [Microsoft TV Technologies], put_LPInnerFEC method [Microsoft TV Technologies],IDVBTLocator interface, tuner/IDVBTLocator::put_LPInnerFEC
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
 - IDVBTLocator.put_LPInnerFEC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVBTLocator::put_LPInnerFEC


## -description



The <b>put_LPInnerFEC</b> method sets the inner FEC type of the low-priority stream.




## -parameters




### -param FEC [in]

Variable of type <a href="https://msdn.microsoft.com/6910c51d-4176-49a3-be6b-6b072ad03fc1">FECMethod</a> that specifies the FEC type.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/f5a95a68-fee0-404c-b9c6-6b808977f8d2">IDVBTLocator Interface</a>
 

 

