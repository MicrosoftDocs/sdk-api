---
UID: NF:mbnapi.IMbnRadioEvents.OnRadioStateChange
title: IMbnRadioEvents::OnRadioStateChange (mbnapi.h)
author: windows-sdk-content
description: A notification signaling that the radio state of the device has changed.
old-location: mbn\imbnradioevents_onradiostatechange.htm
tech.root: mbn
ms.assetid: ae7bf0d0-333b-429d-9dd1-9580745aad35
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnRadioEvents interface [Microsoft Broadband Networks],OnRadioStateChange method, IMbnRadioEvents.OnRadioStateChange, IMbnRadioEvents::OnRadioStateChange, OnRadioStateChange, OnRadioStateChange method [Microsoft Broadband Networks], OnRadioStateChange method [Microsoft Broadband Networks],IMbnRadioEvents interface, mbn.imbnradioevents_onradiostatechange, mbnapi/IMbnRadioEvents::OnRadioStateChange
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - IMbnRadioEvents.OnRadioStateChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnRadioEvents::OnRadioStateChange


## -description


A notification signaling that the radio state of the device has changed.


## -parameters




### -param newInterface [in]

Pointer to an <a href="https://msdn.microsoft.com/b4b5ccfc-6cbf-4090-aee1-ee97092147f7">IMbnRadio</a> interface representing the device for which the radio state has changed.


## -returns



This method must return <b>S_OK</b>.




## -remarks



New software and hardware radio states can be obtained from the passed <i>newInterface</i> object.




## -see-also




<a href="https://msdn.microsoft.com/f02fa823-c1ca-4867-981d-cb3107f7291b">IMbnRadioEvents</a>
 

 

