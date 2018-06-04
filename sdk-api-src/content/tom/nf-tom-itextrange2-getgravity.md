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

# ITextRange2::GetGravity


## -description


Gets the gravity of this range.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The gravity value, which can be one of the following: 

<a id="tomGravityUI"></a>
<a id="tomgravityui"></a>
<a id="TOMGRAVITYUI"></a>


#### tomGravityUI

<a id="tomGravityBack"></a>
<a id="tomgravityback"></a>
<a id="TOMGRAVITYBACK"></a>


#### tomGravityBack

<a id="tomGravityFore"></a>
<a id="tomgravityfore"></a>
<a id="TOMGRAVITYFORE"></a>


#### tomGravityFore

<a id="tomGravityIn"></a>
<a id="tomgravityin"></a>
<a id="TOMGRAVITYIN"></a>


#### tomGravityIn

<a id="tomGravityOut"></a>
<a id="tomgravityout"></a>
<a id="TOMGRAVITYOUT"></a>


#### tomGravityOut


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/10214543-36da-46e3-b926-0ba088f84a7b">ITextRange2::SetGravity</a>
 

 

