---
UID: NF:tuner.IESValueUpdatedEvent.GetValueNames
title: IESValueUpdatedEvent::GetValueNames (tuner.h)
author: windows-sdk-content
description: For a name-value pair in the PBDA General Purpose Name-Value Service, gets the name for the value that has been updated.
old-location: mstv\iesvalueupdatedevent_getvaluenames.htm
tech.root: mstv
ms.assetid: bc008b4a-fa6f-4b62-90da-417813081344
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetValueNames, GetValueNames method [Microsoft TV Technologies], GetValueNames method [Microsoft TV Technologies],IESValueUpdatedEvent interface, IESValueUpdatedEvent interface [Microsoft TV Technologies],GetValueNames method, IESValueUpdatedEvent.GetValueNames, IESValueUpdatedEvent::GetValueNames, mstv.iesvalueupdatedevent_getvaluenames, tuner/IESValueUpdatedEvent::GetValueNames
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IESValueUpdatedEvent.GetValueNames
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IESValueUpdatedEvent::GetValueNames


## -description


For a name-value pair in the PBDA General Purpose Name-Value Service, gets the name for the value that has been updated. PBDA Media Sink Devices (MSDs) get this name from <b>ValueUpdated</b> events fired by Media Transform Devices (MTDs) that implement the <a href="https://msdn.microsoft.com/6639c483-aebe-43b4-94cd-494b820c1b14">IESValueUpdatedEvent</a> interface.


## -parameters




### -param pbstrNames [out, retval]

Pointer to a buffer that gets the name that has been updated. The caller is responsible for freeing this memory.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6639c483-aebe-43b4-94cd-494b820c1b14">IESValueUpdatedEvent</a>
 

 

