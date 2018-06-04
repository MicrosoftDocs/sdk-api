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

# IFECommon::IsDefaultIME


## -description


Determines if the IME specified by the class ID is the default IME on a local computer.

The name of the IME is obtained from the  <a href="https://msdn.microsoft.com/731b8209-1ca8-4667-bd39-7bd0cef45380">Win32 keyboard layout API</a>.


## -parameters




### -param szName [out]

The name of the IME for the specified class ID. Can be <b>NULL</b>.


### -param cszName [in]

The size of <i>szName</i> in bytes.


## -returns



<ul>
<li><b>S_OK</b> if this Microsoft IME is already the default IME.</li>
<li><b>
S_FALSE</b> if this Microsoft IME is not the default IME.</li>
<li>Otherwise <b>E_FAIL</b>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/9FBECA6F-F162-485D-938F-FADC2D47083E">IFECommon</a>



<a href="https://msdn.microsoft.com/731b8209-1ca8-4667-bd39-7bd0cef45380">Win32 keyboard layout API</a>
 

 

