---
UID: NS:evcode.AM_WMT_EVENT_DATA
title: AM_WMT_EVENT_DATA
author: windows-driver-content
description: The AM_WMT_EVENT_DATA structure contains information pertaining to a EC_WMT_EVENT event.
old-location: dshow\am_wmt_event_data.htm
old-project: DirectShow
ms.assetid: d28efe7f-b1ff-4454-8779-95851a86c94a
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: AM_WMT_EVENT_DATA, AM_WMT_EVENT_DATA structure [DirectShow], AM_WMT_EVENT_DATAStructure, dshow.am_wmt_event_data, evcode/AM_WMT_EVENT_DATA
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: evcode.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AM_WMT_EVENT_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	evcode.h
api_name:
-	AM_WMT_EVENT_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# AM_WMT_EVENT_DATA structure


## -description



The AM_WMT_EVENT_DATA structure contains information pertaining to a <a href="https://msdn.microsoft.com/ac6ea7a1-238e-42ae-9f10-e1db60381357">EC_WMT_EVENT</a> event.




## -struct-fields




### -field hrStatus

The status code returned by the Windows Media Format SDK.


### -field pData

Pointer whose data is dependent on the value of the <a href="https://msdn.microsoft.com/ebf77e8a-65e8-4da9-bb21-a1e2bf427bbf">WMT_STATUS</a> message in <i>lParam1</i> of the <a href="https://msdn.microsoft.com/ac6ea7a1-238e-42ae-9f10-e1db60381357">EC_WMT_EVENT</a> event.


## -remarks



This structure is relevant when using the <a href="https://msdn.microsoft.com/82b9f849-b9dc-439b-8ca7-9dcd992338ab">WM ASF Reader</a> filter to read files protected with Digital Rights Management.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

