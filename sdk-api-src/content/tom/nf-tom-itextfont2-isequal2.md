---
UID: NF:tom.ITextFont2.IsEqual2
title: ITextFont2::IsEqual2
author: windows-sdk-content
description: Determines whether this text font object has the same properties as the specified text font object.
old-location: controls\itextfont2_isequal2.htm
tech.root: Controls
ms.assetid: c423bbdb-a108-4f29-8dc4-3dd35849f39a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextFont2 interface [Windows Controls],IsEqual2 method, ITextFont2.IsEqual2, ITextFont2::IsEqual2, IsEqual2, IsEqual2 method [Windows Controls], IsEqual2 method [Windows Controls],ITextFont2 interface, controls.itextfont2_isequal2, tom/ITextFont2::IsEqual2
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
 - ITextFont2.IsEqual2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont2::IsEqual2


## -description


Determines whether this text font object has the same properties as the specified text font object.


## -parameters




### -param pFont [in]

Type: <b><a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>*</b>

The text font object to compare against.


### -param pB [out]

Type: <b>long*</b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb787873(v=VS.85).aspx">tomBool</a> value that is <b>tomTrue</b> if the font objects have the same properties, or <b>tomFalse</b> if they don't. This parameter can be <b>NULL</b>. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



 For two text font objects to be equal, both must belong to the same Text Object Model (TOM) object. 

The <b>ITextFont::IsEqual2</b> method ignores entries for which either font object has a <a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomUndefined</a> value.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787863(v=VS.85).aspx">ITextFont::IsEqual</a>
 

 

