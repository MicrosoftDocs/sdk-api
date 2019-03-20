---
UID: NF:winevt.EvtNextEventMetadata
title: EvtNextEventMetadata function (winevt.h)
author: windows-sdk-content
description: Gets an event definition from the enumerator.
old-location: wes\evtnexteventmetadata.htm
tech.root: wes
ms.assetid: 1077dc7c-3e73-4135-9020-20d086e30e71
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EvtNextEventMetadata, EvtNextEventMetadata function [EventLog], wes.evtnexteventmetadata, winevt/EvtNextEventMetadata
ms.topic: function
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
api_name:
 - EvtNextEventMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtNextEventMetadata function


## -description


Gets an event definition from the enumerator.


## -parameters




### -param EventMetadataEnum [in]

A handle to the event definition enumerator that the <a href="https://msdn.microsoft.com/e1d2e5d5-89db-4bda-9803-37f26d1fe30f">EvtOpenEventMetadataEnum</a> function returns.


### -param Flags [in]

Reserved. Must be zero.


## -returns



If successful, the function returns a handle to the event's metadata; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.




## -remarks



Call this function in a loop until the function returns <b>NULL</b> and the error code is ERROR_NO_MORE_ITEMS.

To get a property from the event definition, call the <a href="https://msdn.microsoft.com/2a5c53e3-bbb4-4245-a640-86b58d1a3c52">EvtGetEventMetadataProperty</a> function.

You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function to close the event definition handle when done.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/c9442dc1-3599-4e81-a144-943c2843a2f7">Getting a Provider's Metadata</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2a5c53e3-bbb4-4245-a640-86b58d1a3c52">EvtGetEventMetadataProperty</a>
 

 

