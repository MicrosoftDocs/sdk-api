---
UID: NF:tom.ITextRow.IsEqual
title: ITextRow::IsEqual
author: windows-sdk-content
description: Compares two table rows to determine if they have the same properties.
old-location: controls\itextrow_isequal.htm
old-project: Controls
ms.assetid: 2e516a4d-0f3b-475b-969d-661662bfaeef
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ITextRow interface [Windows Controls],IsEqual method, ITextRow.IsEqual, ITextRow::IsEqual, IsEqual, IsEqual method [Windows Controls], IsEqual method [Windows Controls],ITextRow interface, controls.itextrow_isequal, tom/ITextRow::IsEqual
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
-	ITextRow.IsEqual
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRow::IsEqual


## -description


Compares two table rows to determine if they have the same properties.


## -parameters




### -param pRow [in]

Type: <b><a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>*</b>

The row to compare to.


### -param pB [out, retval]

Type: <b>long*</b>

 The comparison result. The value is set to  <b>tomTrue</b> if equal, and <b>tomFalse</b> if not. The value can be <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>
 

 

