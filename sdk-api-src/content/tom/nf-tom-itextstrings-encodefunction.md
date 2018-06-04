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

# ITextStrings::EncodeFunction


## -description


Encodes an object, given a set of argument strings.


## -parameters




### -param Type [in]

Type: <b>long</b>

The object type. See <a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">ITextRange2::GetInlineObject</a> for a table of definitions.


### -param Align [in]

Type: <b>long</b>

The object alignment. See <a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">ITextRange2::GetInlineObject</a> for a table of definitions.


### -param Char [in]

Type: <b>long</b>

The object character.


### -param Char1 [in]

Type: <b>long</b>

The object character.


### -param Char2 [in]

Type: <b>long</b>

The object character.


### -param Count [in]

Type: <b>long</b>

The count of strings (arguments) to concatenate.


### -param TeXStyle [in]

Type: <b>long</b>

The TeX style.


### -param cCol [in]

Type: <b>long</b>

The count of columns (<b>tomArray</b> only).


### -param pRange [in]

Type: <b><a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>*</b>

The specifying range that points at the desired formatting.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



See <a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">ITextRange2::GetInlineObject</a> for a more detailed discussion of the arguments.




## -see-also




<a href="https://msdn.microsoft.com/c878d0db-ac13-4ac9-8601-d1c1ba76cd85">ITextStrings</a>
 

 

