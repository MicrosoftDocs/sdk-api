---
UID: NF:comsvcs.IMtsEventInfo.get_EventID
title: IMtsEventInfo::get_EventID (comsvcs.h)
description: Retrieves the event identifier of the object.
helpviewer_keywords: ["IMtsEventInfo interface [COM+]","get_EventID method","IMtsEventInfo.get_EventID","IMtsEventInfo::get_EventID","_dtc_IMtsEventInfo_EventID","comsvcs/IMtsEventInfo::get_EventID","cos.imtseventinfo_get_eventid","get_EventID","get_EventID method [COM+]","get_EventID method [COM+]","IMtsEventInfo interface"]
old-location: cos\imtseventinfo_get_eventid.htm
tech.root: cos
ms.assetid: 20695360-ed0d-4d8b-8c3b-42adc42e87b3
ms.date: 12/05/2018
ms.keywords: IMtsEventInfo interface [COM+],get_EventID method, IMtsEventInfo.get_EventID, IMtsEventInfo::get_EventID, _dtc_IMtsEventInfo_EventID, comsvcs/IMtsEventInfo::get_EventID, cos.imtseventinfo_get_eventid, get_EventID, get_EventID method [COM+], get_EventID method [COM+],IMtsEventInfo interface
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMtsEventInfo::get_EventID
 - comsvcs/IMtsEventInfo::get_EventID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMtsEventInfo.get_EventID
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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtseventinfo">IMtsEventInfo</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsevents">IMtsEvents</a>