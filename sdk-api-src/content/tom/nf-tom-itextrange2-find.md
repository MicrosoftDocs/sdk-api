---
UID: NF:tom.ITextRange2.Find
title: ITextRange2::Find
author: windows-sdk-content
description: Searchs for math inline functions in text as specified by a source range.
old-location: controls\itextrange2_find.htm
old-project: controls
ms.assetid: 4935d322-016a-4c08-858e-42009a9f59f1
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: Find, Find method [Windows Controls], Find method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],Find method, ITextRange2.Find, ITextRange2::Find, controls.itextrange2_find, tom/ITextRange2::Find
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
 - ITextRange2.Find
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange2::Find


## -description


Searchs for math inline functions in text as specified by a source range.


## -parameters




### -param pRange [in]

Type: <b><a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>*</b>

The formatted text to find in the range's text.


### -param Count [in]

Type: <b>long</b>

The number of characters to search through.


### -param Flags [in]

Type: <b>long</b>

Flags that control the search as defined for <a href="https://msdn.microsoft.com/library/Bb787783(v=VS.85).aspx">ITextRange::FindText</a>.


### -param pDelta [out]

Type: <b>long*</b>

A count of the number of characters bypassed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If the string is found, and the math inline functions, if any, are the same as their counterparts in the source range, the range limits are changed to be those of the matched string and length is set equal to the length of the string. 

If the string isn't found, the range remains unchanged and length is set equal to 0.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

