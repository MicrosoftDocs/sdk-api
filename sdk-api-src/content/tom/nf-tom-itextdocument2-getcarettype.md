---
UID: NF:tom.ITextDocument2.GetCaretType
title: ITextDocument2::GetCaretType
author: windows-sdk-content
description: Gets the caret type.
old-location: controls\itextdocument2_getcarettype.htm
old-project: Controls
ms.assetid: 4ab170d2-50a3-4fbf-8e02-92b031bc1e4f
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetCaretType, GetCaretType method [Windows Controls], GetCaretType method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetCaretType method, ITextDocument2.GetCaretType, ITextDocument2::GetCaretType, controls.itextdocument2_getcarettype, tom/ITextDocument2::GetCaretType, tomKoreanBlockCaret, tomNormalCaret, tomNullCaret
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument2.GetCaretType
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::GetCaretType


## -description


Gets the caret type.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The caret type. It can be one of the following values:

<a id="tomKoreanBlockCaret"></a>
<a id="tomkoreanblockcaret"></a>
<a id="TOMKOREANBLOCKCARET"></a>


#### tomKoreanBlockCaret

<a id="tomNormalCaret"></a>
<a id="tomnormalcaret"></a>
<a id="TOMNORMALCARET"></a>


#### tomNormalCaret

<a id="tomNullCaret"></a>
<a id="tomnullcaret"></a>
<a id="TOMNULLCARET"></a>


#### tomNullCaret


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/40d34482-cf07-4401-ad02-f5d1b0184976">ITextDocument2::SetCaretType</a>
 

 

