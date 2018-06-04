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

# ITextFont2::SetUnderlinePositionMode


## -description


Sets the underline position mode.


## -parameters




### -param Value [in]

Type: <b>long</b>

The new underline position mode. It can be one of the following values.<ul>
<li><a href="tomconstants.htm">tomUnderlinePositionAuto</a> (the default)</li>
<li><a href="tomconstants.htm">tomUnderlinePositionBelow</a></li>
<li><a href="tomconstants.htm">tomUnderlinePositionAbove</a></li>
</ul>



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/cd7a45be-05b0-4a43-90c8-0fd8393794c0">ITextFont2::GetUnderlinePositionMode</a>
 

 

