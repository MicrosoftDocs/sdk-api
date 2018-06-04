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

# ITextRange2::SetInlineObject


## -description


Sets or inserts the properties of an inline object for a degenerate range.


## -parameters




### -param Type [in]

Type: <b>long</b>

The object type as defined in <a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">ITextRange2::GetInlineObject</a>.


### -param Align [in]

Type: <b>long</b>

The object alignment as defined in <a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">ITextRange2::GetInlineObject</a>.


### -param Char [in]

Type: <b>long</b>

The object character as defined in <a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">ITextRange2::GetInlineObject</a>.


### -param Char1 [in]

Type: <b>long</b>

The closing bracket (<a href="objecttype.htm">tomBrackets</a>) character. See <a href="http://go.microsoft.com/fwlink/p/?linkid=124972">Unicode Technical Note 28</a> for a list of characters.


### -param Char2 [in]

Type: <b>long</b>

The separator character for <a href="objecttype.htm">tomBracketsWithSeps</a>, which can be one of the following values.


### -param Count [in]

Type: <b>long</b>

The number of arguments in the inline object.


### -param TeXStyle [in]

Type: <b>long</b>

The TeX style, as defined in <a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">ITextRange2::GetInlineObject</a>.


### -param cCol [in]

Type: <b>long</b>

The number of columns in the inline object. For  <a href="objecttype.htm">tomMatrix</a> only.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">ITextRange2::GetInlineObject</a>
 

 

