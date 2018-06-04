---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _MFP_CREATION_OPTIONS enumeration


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Specifies options for the <a href="https://msdn.microsoft.com/80c668e2-5e93-4af2-871c-646228e18717">MFPCreateMediaPlayer</a> function.


## -enum-fields




### -field MFP_OPTION_NONE

Use the default creation options.


### -field MFP_OPTION_FREE_THREADED_CALLBACK

If set, the MFPlay player object invokes the application's <a href="https://msdn.microsoft.com/7d9d01bf-861a-4c35-93b1-dbf85cbf0a32">IMFPMediaPlayerCallback</a> callback on another thread, and not the thread that called the <a href="https://msdn.microsoft.com/80c668e2-5e93-4af2-871c-646228e18717">MFPCreateMediaPlayer</a> function. Therefore, the callback must be thread safe.

If this flag is not set, the player object invokes the callback on the same thread that calls <a href="https://msdn.microsoft.com/80c668e2-5e93-4af2-871c-646228e18717">MFPCreateMediaPlayer</a>. This thread must have a message loop. Internally, the player object creates a hidden window to dispatch the callback, similar to the mechanism used for single-threaded apartments (STAs) in COM.


### -field MFP_OPTION_NO_MMCSS

Do not register the playback topology with the Multimedia Class Scheduler Service (MMCSS). By default, the MFPlay object registers the playback topology with MMCSS, which typically results in a better playback experience. For more information, see <a href="https://msdn.microsoft.com/7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d">IMFWorkQueueServices</a>.


### -field MFP_OPTION_NO_REMOTE_DESKTOP_OPTIMIZATION

Disables optimizations that are otherwise performed when the application runs in a Remote Desktop Services (RDS, formerly Terminal Services) environment.


## -remarks



The following <b>typedef</b> is defined for combining flags from this enumeration.

<pre class="syntax" xml:space="preserve"><code>typedef UINT32 MFP_CREATION_OPTIONS;</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

