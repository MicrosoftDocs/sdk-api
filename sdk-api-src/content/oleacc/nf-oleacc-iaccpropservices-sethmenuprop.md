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

# IAccPropServices::SetHmenuProp


## -description


This method wraps <a href="https://msdn.microsoft.com/c86acb70-fa77-4f95-8a99-e60872cdaa7e">SetPropValue</a>, providing a convenient entry point for callers who are annotating <b>HMENU</b>-based accessible elements. If the new value is a string, you can use <a href="https://msdn.microsoft.com/891af40a-819b-4fce-a1bb-28db145b87f1">IAccPropServices::SetHmenuPropStr</a> instead.


## -parameters




### -param hmenu [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMENU</a></b>

Identifies the <b>HMENU</b>-based accessible element to be annotated.


### -param idChild [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the child ID of the accessible element.


### -param idProp [in]

Type: <b>MSAAPROPID</b>

Specifies which property of the accessible element is to be annotated.


### -param var [in]

Type: <b>VARIANT</b>

Specifies a new value for the <i>idProp</i> property.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

May return other error codes under exceptional error conditions such as low memory.




## -see-also




<a href="https://msdn.microsoft.com/dbff74b0-c67b-4ef4-add7-6063c4760455">ClearHmenuProps</a>



<a href="https://msdn.microsoft.com/0474dacf-7aa1-4d12-bac2-1091676a1ced">IAccPropServices</a>



<a href="https://msdn.microsoft.com/7bc91ee3-f0ea-43d5-a8b7-d1444c53cd14">SetHmenuPropServer</a>



<a href="https://msdn.microsoft.com/891af40a-819b-4fce-a1bb-28db145b87f1">SetHmenuPropStr</a>



<a href="https://msdn.microsoft.com/c86acb70-fa77-4f95-8a99-e60872cdaa7e">SetPropValue</a>
 

 

