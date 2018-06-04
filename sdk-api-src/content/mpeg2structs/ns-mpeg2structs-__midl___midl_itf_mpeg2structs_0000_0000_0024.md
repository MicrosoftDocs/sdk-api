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

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0024 structure


## -description



The <b>MPEG_TIME</b> structure represents a time of day, or a duration.




## -struct-fields




### -field Hours

Specifies the hours. The value can range from 0 to 23, inclusive.


### -field Minutes

Specifies the minutes. The value can range from 0 to 59, inclusive.


### -field Seconds

Specifies the seconds. The value can range from 0 to 59, inclusive.


## -remarks



The <b>MPEG_DURATION</b> structure is a <code>typedef</code> for the <b>MPEG_TIME</b> structure.

<pre class="syntax" xml:space="preserve"><code>typedef MPEG_TIME MPEG_DURATION;</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>
 

 

