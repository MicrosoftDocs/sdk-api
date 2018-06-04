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

# ITextDocument2::SetEffectColor


## -description


Specifies the color to use for special text attributes.


## -parameters




### -param Index [in]

Type: <b>long</b>

The index of the color to retrieve. For a list of values, see <a href="https://msdn.microsoft.com/4bc2740e-852f-430b-913e-5d28baec3272">GetEffectColor</a>.


### -param Value [in]

Type: <b>long</b>

The new color for the specified index.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The first 16 index values are for special underline colors. If an index between 1 and 16 hasn't been defined by a call to the <b>ITextDocument2:SetEffectColor</b> method, the corresponding Microsoft Word default color is used. 




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/4bc2740e-852f-430b-913e-5d28baec3272">ITextDocument2::GetEffectColor</a>
 

 

