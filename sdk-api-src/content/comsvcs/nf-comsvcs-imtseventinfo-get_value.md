---
UID: NF:comsvcs.IMtsEventInfo.get_Value
title: IMtsEventInfo::get_Value
author: windows-sdk-content
description: Retrieves the value of the specified user-defined event.
old-location: cos\imtseventinfo_get_value.htm
tech.root: cossdk
ms.assetid: 61757e85-28b2-4599-9be4-69a3531e5ac2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMtsEventInfo interface [COM+],get_Value method, IMtsEventInfo.get_Value, IMtsEventInfo::get_Value, _dtc_IMtsEventInfo_Value, comsvcs/IMtsEventInfo::get_Value, cos.imtseventinfo_get_value, get_Value, get_Value method [COM+], get_Value method [COM+],IMtsEventInfo interface
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMtsEventInfo.get_Value
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMtsEventInfo::get_Value


## -description


Retrieves the value of the specified user-defined event.


## -parameters




### -param sKey [in]

The name or ordinal of the value.


### -param pVal [out]

The value of the user-defined event.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/9508df6d-281b-4a02-bb95-233b369b8279">IMtsEventInfo</a>



<a href="https://msdn.microsoft.com/7db3a373-00d3-480e-8f8e-7e65a468d5dc">IMtsEvents</a>
 

 

