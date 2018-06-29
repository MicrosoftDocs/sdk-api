---
UID: NF:tom.ITextRow.GetAlignment
title: ITextRow::GetAlignment
author: windows-sdk-content
description: Gets the horizontal alignment of a row.
old-location: controls\itextrow_getalignment.htm
old-project: Controls
ms.assetid: 2c7279b0-6329-4abd-a719-da4ed4d71c71
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetAlignment, GetAlignment method [Windows Controls], GetAlignment method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetAlignment method, ITextRow.GetAlignment, ITextRow::GetAlignment, controls.itextrow_getalignment, tom/ITextRow::GetAlignment
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
 - ITextRow.GetAlignment
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRow::GetAlignment


## -description


Gets the horizontal alignment of a row.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The horizontal alignment. It can be one of the following values.

<p class="indent"><a href="https://msdn.microsoft.com/library/Hh768766(v=VS.85).aspx">tomAlignLeft</a>

<p class="indent"><a href="https://msdn.microsoft.com/library/Hh768766(v=VS.85).aspx">tomAlignCenter</a>

<p class="indent"><a href="https://msdn.microsoft.com/library/Hh768766(v=VS.85).aspx">tomAlignRight</a>


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/bfcc900d-2bec-4314-a2c5-09f55e27a626">ITextRow::SetAlignment</a>
 

 

