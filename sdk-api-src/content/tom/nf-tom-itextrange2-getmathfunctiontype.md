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

# ITextRange2::GetMathFunctionType


## -description


Retrieves the math function type associated with the specified math function name.


## -parameters




### -param bstr [in]

Type: <b>BSTR</b>

The math function name that is checked to determine the math function type.


### -param pValue [out]

Type: <b>long*</b>

The math function type of the function name specified by  <i>bstr</i>. It can be one of the following values.

<a id="tomFunctionTypeNone"></a>
<a id="tomfunctiontypenone"></a>
<a id="TOMFUNCTIONTYPENONE"></a>


#### tomFunctionTypeNone

<a id="tomFunctionTypeTakesArg"></a>
<a id="tomfunctiontypetakesarg"></a>
<a id="TOMFUNCTIONTYPETAKESARG"></a>


#### tomFunctionTypeTakesArg

<a id="tomFunctionTypeTakesLim"></a>
<a id="tomfunctiontypetakeslim"></a>
<a id="TOMFUNCTIONTYPETAKESLIM"></a>


#### tomFunctionTypeTakesLim

<a id="tomFunctionTypeTakesLim2"></a>
<a id="tomfunctiontypetakeslim2"></a>
<a id="TOMFUNCTIONTYPETAKESLIM2"></a>


#### tomFunctionTypeTakesLim2

<a id="tomFunctionTypeIsLim"></a>
<a id="tomfunctiontypeislim"></a>
<a id="TOMFUNCTIONTYPEISLIM"></a>


#### tomFunctionTypeIsLim


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

