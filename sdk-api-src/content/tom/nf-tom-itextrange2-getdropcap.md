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

# ITextRange2::GetDropCap


## -description


Not implemented.

Gets the drop-cap parameters of the paragraph that contains this range.


## -parameters




### -param pcLine [out]

Type: <b>long*</b>

The count of lines for the drop cap.  A value of 0 means no drop cap.


### -param pPosition [out]

Type: <b>long*</b>

The position of the drop cap. The position can be one of the following: 

<ul>
<li>tomDropMargin</li>
<li>tomDropNone</li>
<li>tomDropNormal</li>
</ul>

## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/189c1a69-44eb-4de0-8ffc-9a026d9e6f16">ITextRange2::SetDropCap</a>
 

 

