---
UID: NF:tom.ITextRange2.SetInlineObject
title: ITextRange2::SetInlineObject
author: windows-sdk-content
description: Sets or inserts the properties of an inline object for a degenerate range.
old-location: controls\itextrange2_setinlineobject.htm
tech.root: controls
ms.assetid: 56876a42-a972-4a19-a8f7-a5e37c0d77f0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextRange2 interface [Windows Controls],SetInlineObject method, ITextRange2.SetInlineObject, ITextRange2::SetInlineObject, SetInlineObject, SetInlineObject method [Windows Controls], SetInlineObject method [Windows Controls],ITextRange2 interface, controls.itextrange2_setinlineobject, tom/ITextRange2::SetInlineObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange2.SetInlineObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The closing bracket (<a href="https://msdn.microsoft.com/en-us/library/Hh768758(v=VS.85).aspx">tomBrackets</a>) character. See <a href="http://go.microsoft.com/fwlink/p/?linkid=124972">Unicode Technical Note 28</a> for a list of characters.


### -param Char2 [in]

Type: <b>long</b>

The separator character for <a href="https://msdn.microsoft.com/en-us/library/Hh768758(v=VS.85).aspx">tomBracketsWithSeps</a>, which can be one of the following values.


### -param Count [in]

Type: <b>long</b>

The number of arguments in the inline object.


### -param TeXStyle [in]

Type: <b>long</b>

The TeX style, as defined in <a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">ITextRange2::GetInlineObject</a>.


### -param cCol [in]

Type: <b>long</b>

The number of columns in the inline object. For  <a href="https://msdn.microsoft.com/en-us/library/Hh768758(v=VS.85).aspx">tomMatrix</a> only.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">ITextRange2::GetInlineObject</a>
 

 

