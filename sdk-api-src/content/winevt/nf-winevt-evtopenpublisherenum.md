---
UID: NF:winevt.EvtOpenPublisherEnum
title: EvtOpenPublisherEnum function
author: windows-sdk-content
description: Gets a handle that you use to enumerate the list of registered providers on the computer.
old-location: wes\evtopenpublisherenum.htm
old-project: WES
ms.assetid: 156c434c-6d0f-4af0-bf10-20aa6bae0945
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EvtOpenPublisherEnum, EvtOpenPublisherEnum function [EventLog], wes.evtopenpublisherenum, winevt/EvtOpenPublisherEnum
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EVT_VARIANT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
api_name:
 - EvtOpenPublisherEnum
product: Windows
targetos: Windows
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EvtOpenPublisherEnum function


## -description


Gets a handle that you use to enumerate the list of registered providers on the computer.


## -parameters




### -param Session [in]

A remote session handle that the <a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a> function returns. Set to <b>NULL</b> to enumerate the registered providers on the local computer.


### -param Flags [in]

Reserved. Must be zero.


## -returns



If successful, the function returns a handle to the list of registered providers; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.




## -remarks



To enumerate the registered providers, call the <a href="https://msdn.microsoft.com/e6cea6de-79f3-416b-9501-8d86f2579aa8">EvtNextPublisherId</a> function in a loop.

You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function to close the enumerator handle when done.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/c9442dc1-3599-4e81-a144-943c2843a2f7">Getting a Provider's Metadata</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e6cea6de-79f3-416b-9501-8d86f2579aa8">EvtNextPublisherId</a>
 

 

