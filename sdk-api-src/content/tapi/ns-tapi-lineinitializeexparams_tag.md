---
UID: NS:tapi.lineinitializeexparams_tag
title: lineinitializeexparams_tag
author: windows-sdk-content
description: The LINEINITIZALIZEEXPARAMS structure describes parameters supplied when making calls using LINEINITIALIZEEX.
old-location: tapi2\lineinitializeexparams_str.htm
tech.root: tapi
ms.assetid: 17fed282-6d08-4702-9ceb-9cbcc3737395
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPLINEINITIALIZEEXPARAMS, LINEINITIALIZEEXPARAMS, LINEINITIALIZEEXPARAMS structure [TAPI 2.2], LPLINEINITIALIZEEXPARAMS, LPLINEINITIALIZEEXPARAMS structure pointer [TAPI 2.2], _tapi2_lineinitializeexparams_str, lineinitializeexparams_tag, tapi/LINEINITIALIZEEXPARAMS, tapi/LPLINEINITIALIZEEXPARAMS, tapi2.lineinitializeexparams_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEINITIALIZEEXPARAMS
product: Windows
targetos: Windows
req.typenames: LINEINITIALIZEEXPARAMS, *LPLINEINITIALIZEEXPARAMS
req.redist: 
---

# lineinitializeexparams_tag structure


## -description


The <b>LINEINITIZALIZEEXPARAMS</b> structure describes parameters supplied when making calls using 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">LINEINITIALIZEEX</a>.


## -struct-fields




### -field dwTotalSize

Total size, in bytes, allocated to this data structure.


### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwOptions

One of the 
<a href="https://msdn.microsoft.com/77674a45-7133-4518-af47-a9d58392b80b">LINEINITIALIZEEXOPTION_ Constants</a>. Specifies the event notification mechanism the application desires to use.


### -field Handles


### -field Handles.hEvent

If <b>dwOptions</b> specifies LINEINITIALIZEEXOPTION_USEEVENT, TAPI returns the event handle in this field.


### -field Handles.hCompletionPort

If <b>dwOptions</b> specifies LINEINITIALIZEEXOPTION_USECOMPLETIONPORT, the application must specify in this field the handle of an existing completion port opened using 
<a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a>.


### -field dwCompletionKey

If <b>dwOptions</b> specifies LINEINITIALIZEEXOPTION_USECOMPLETIONPORT, the application must specify in this field a value that is returned through the <i>lpCompletionKey</i> parameter of 
<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> to identify the completion message as a telephony message.


## -remarks



See 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a> for further information on these options.




## -see-also




<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>
 

 

