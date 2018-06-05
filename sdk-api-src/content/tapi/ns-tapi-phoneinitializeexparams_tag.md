---
UID: NS:tapi.phoneinitializeexparams_tag
title: phoneinitializeexparams_tag
author: windows-sdk-content
description: The PHONEINITIALIZEEXPARAMS structure contains parameters used to establish the association between an application and TAPI; for example, the application's selected event notification mechanism. The phoneInitializeEx function uses this structure.
old-location: tapi2\phoneinitializeexparams_str.htm
old-project: Tapi
ms.assetid: 465653e4-b88a-42a0-99b0-ce26eeaf99fd
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*LPPHONEINITIALIZEEXPARAMS, LPPHONEINITIALIZEEXPARAMS, LPPHONEINITIALIZEEXPARAMS structure pointer [TAPI 2.2], PHONEINITIALIZEEXPARAMS, PHONEINITIALIZEEXPARAMS structure [TAPI 2.2], _tapi2_phoneinitializeexparams_str, phoneinitializeexparams_tag, tapi/LPPHONEINITIALIZEEXPARAMS, tapi/PHONEINITIALIZEEXPARAMS, tapi2.phoneinitializeexparams_str"
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
tech.root: 
req.typenames: PHONEINITIALIZEEXPARAMS, *LPPHONEINITIALIZEEXPARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi.h
api_name:
-	PHONEINITIALIZEEXPARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneinitializeexparams_tag structure


## -description


The 
<b>PHONEINITIALIZEEXPARAMS</b> structure contains parameters used to establish the association between an application and TAPI; for example, the application's selected event notification mechanism. The 
<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a> function uses this structure.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwOptions

One of the 
<a href="https://msdn.microsoft.com/7d8b122d-bebe-4904-abc8-d680b0899e25">PHONEINITIALIZEEXOPTION_ Constants</a>. Specifies the event notification mechanism the application desires to use.


### -field Handles


### -field Handles.hEvent

If <b>dwOptions</b> specifies PHONEINITIALIZEEXOPTION_USEEVENT, TAPI returns the event handle in this member.


### -field Handles.hCompletionPort

If <b>dwOptions</b> specifies PHONEINITIALIZEEXOPTION_USECOMPLETIONPORT, the application must specify in this member the handle of an existing completion port opened using 
<a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a>.


### -field dwCompletionKey

If <b>dwOptions</b> specifies PHONEINITIALIZEEXOPTION_USECOMPLETIONPORT, the application must specify in this field a value that is returned through the <i>lpCompletionKey</i> parameter of 
<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> to identify the completion message as a telephony message.


## -remarks



See 
<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a> for further information on these options.




## -see-also




<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a>
 

 

