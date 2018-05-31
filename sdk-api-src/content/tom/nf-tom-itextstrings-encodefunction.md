---
UID: NF:tom.ITextStrings.EncodeFunction
title: ITextStrings::EncodeFunction
author: windows-sdk-content
description: Encodes an object, given a set of argument strings.
old-location: controls\itextstrings_encodefunction.htm
old-project: Controls
ms.assetid: f22bb343-4fcc-4473-84cc-807011b5a7b0
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: EncodeFunction, EncodeFunction method [Windows Controls], EncodeFunction method [Windows Controls],ITextStrings interface, ITextStrings interface [Windows Controls],EncodeFunction method, ITextStrings.EncodeFunction, ITextStrings::EncodeFunction, controls.itextstrings_encodefunction, tom/ITextStrings::EncodeFunction
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextStrings.EncodeFunction
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

