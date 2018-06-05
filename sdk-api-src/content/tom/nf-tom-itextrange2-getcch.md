---
UID: NF:tom.ITextRange2.GetCch
title: ITextRange2::GetCch
author: windows-sdk-content
description: Gets the count of characters in a range.
old-location: controls\itextrange2_getcch.htm
old-project: Controls
ms.assetid: a6f06062-3c8f-40c0-9b5d-6c22a647bfbc
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetCch, GetCch method [Windows Controls], GetCch method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetCch method, ITextRange2.GetCch, ITextRange2::GetCch, controls.itextrange2_getcch, tom/ITextRange2::GetCch
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextRange2.GetCch
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange2::GetCch


## -description


Gets the count of characters in a range.


## -parameters




### -param pcch [out, retval]

Type: <b>long*</b>

The signed count of characters.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The count of characters is the difference between the character position of the active end of the range, and the character position of the anchor end. Some Text Object Model (TOM) implementations might include active ends only for a selection (represented by the <a href="https://msdn.microsoft.com/e6afce18-4f02-4f1c-a2ee-735465d2e168">ITextSelection</a> interface). The rich edit control's TOM implementation of a text range (represented by the <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a> interface) also has active ends. 




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

