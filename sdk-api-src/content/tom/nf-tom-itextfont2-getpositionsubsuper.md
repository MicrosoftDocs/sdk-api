---
UID: NF:tom.ITextFont2.GetPositionSubSuper
title: ITextFont2::GetPositionSubSuper
author: windows-sdk-content
description: Gets the subscript or superscript position relative to the baseline.
old-location: controls\itextfont2_getpositionsubsuper.htm
tech.root: controls
ms.assetid: c7e53a94-b218-47d1-b366-3bbf7779516e
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: GetPositionSubSuper, GetPositionSubSuper method [Windows Controls], GetPositionSubSuper method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetPositionSubSuper method, ITextFont2.GetPositionSubSuper, ITextFont2::GetPositionSubSuper, controls.itextfont2_getpositionsubsuper, tom/ITextFont2::GetPositionSubSuper
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
 - ITextFont2.GetPositionSubSuper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont2::GetPositionSubSuper


## -description


Gets the subscript or superscript position relative to the baseline.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The subscript or superscript position relative to the baseline.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The subscript or superscript position is relative to the baseline as a percent of the font height.

Subscripts and superscripts in math zones are handled using the <a href="https://msdn.microsoft.com/en-us/library/Hh768758(v=VS.85).aspx">tomSubscript</a>, <a href="https://msdn.microsoft.com/en-us/library/Hh768758(v=VS.85).aspx">tomSuperscript</a>, <a href="https://msdn.microsoft.com/en-us/library/Hh768758(v=VS.85).aspx">tomSubSup</a>, and <a href="https://msdn.microsoft.com/en-us/library/Hh768758(v=VS.85).aspx">tomLeftSubSup</a> mathematical objects. See <a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">ITextRange2::GetInlineObject</a>.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/3f78a91b-17a3-48ff-9ca0-1eb4f9c95be4">ITextFont2::SetPositionSubSuper</a>
 

 

