---
UID: NF:comsvcs.IMtsEventInfo.get_EventID
title: IMtsEventInfo::get_EventID
author: windows-sdk-content
description: Retrieves the event identifier of the object.
old-location: cos\imtseventinfo_get_eventid.htm
old-project: cossdk
ms.assetid: 20695360-ed0d-4d8b-8c3b-42adc42e87b3
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IMtsEventInfo interface [COM+],get_EventID method, IMtsEventInfo.get_EventID, IMtsEventInfo::get_EventID, _dtc_IMtsEventInfo_EventID, comsvcs/IMtsEventInfo::get_EventID, cos.imtseventinfo_get_eventid, get_EventID, get_EventID method [COM+], get_EventID method [COM+],IMtsEventInfo interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMtsEventInfo.get_EventID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMtsEventInfo::get_EventID


## -description


Retrieves the event identifier of the object.


## -parameters




### -param sGuidEventID [out]

The event identifier of the object. This is a GUID converted to a string.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/9508df6d-281b-4a02-bb95-233b369b8279">IMtsEventInfo</a>



<a href="https://msdn.microsoft.com/7db3a373-00d3-480e-8f8e-7e65a468d5dc">IMtsEvents</a>
 

 

