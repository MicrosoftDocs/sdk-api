---
UID: NF:tuner.IATSCLocator.get_TSID
title: IATSCLocator::get_TSID
author: windows-sdk-content
description: The get_TSID method retrieves the transport stream ID.
old-location: mstv\iatsclocator_get_tsid.htm
tech.root: MSTV
ms.assetid: e7cde550-742c-426c-a350-1d05b74f824d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IATSCLocator interface [Microsoft TV Technologies],get_TSID method, IATSCLocator.get_TSID, IATSCLocator::get_TSID, IATSCLocatorget_TSID, get_TSID, get_TSID method [Microsoft TV Technologies], get_TSID method [Microsoft TV Technologies],IATSCLocator interface, mstv.iatsclocator_get_tsid, tuner/IATSCLocator::get_TSID
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
 - IATSCLocator.get_TSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IATSCLocator::get_TSID


## -description



The <b>get_TSID</b> method retrieves the transport stream ID.




## -parameters




### -param TSID

TBD




#### - pTSID [out]

Receives the transport stream ID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This property is not required for tuning. It will be set by the BDA Transport Information Filter (TIF) when the signal is acquired. This property is not used by the application but may be used by one or more of the receiver filters. For example, a TIF may use this to determine whether the transport stream has changed from what was originally tuned and generate events that cause re-acquisition of the requested program.




## -see-also




<a href="https://msdn.microsoft.com/8ca7d50f-e7cc-4938-a2ed-fce5278b73fd">IATSCLocator Interface</a>
 

 

