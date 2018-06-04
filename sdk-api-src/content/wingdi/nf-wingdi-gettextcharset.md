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

# GetTextCharset function


## -description


Retrieves a character set identifier for the font that is currently selected into a specified device context.
<div class="alert"><b>Note</b>  A call to this function is equivalent to a call to <a href="https://msdn.microsoft.com/1c8c114a-b261-457c-b541-4648a8f38ee8">GetTextCharsetInfo</a> passing <b>NULL</b> for the data buffer.</div><div> </div>

## -parameters




### -param hdc [in]

Handle to a device context. The function obtains a character set identifier for the font that is selected into this device context.


## -returns



If successful, returns a value identifying the character set of the font that is currently selected into the specified device context. The following character set identifiers are defined:

If the function fails, it returns DEFAULT_CHARSET.




## -see-also




<a href="https://msdn.microsoft.com/1c8c114a-b261-457c-b541-4648a8f38ee8">GetTextCharsetInfo</a>



<a href="https://msdn.microsoft.com/1799f5da-1391-4b6e-ac13-718017a77557">Unicode and Character Set Functions</a>



<a href="https://msdn.microsoft.com/8c1c6582-b58c-4008-9ce5-208acc191d9f">Unicode and Character Sets</a>
 

 

