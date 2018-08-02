---
UID: NF:tom.ITextFont2.SetUnderlinePositionMode
title: ITextFont2::SetUnderlinePositionMode
author: windows-sdk-content
description: Sets the underline position mode.
old-location: controls\itextfont2_setunderlinepositionmode.htm
old-project: Controls
ms.assetid: 31dff2d0-7165-42f0-b3d0-9cb679c738c3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetUnderlinePositionMode method, ITextFont2.SetUnderlinePositionMode, ITextFont2::SetUnderlinePositionMode, SetUnderlinePositionMode, SetUnderlinePositionMode method [Windows Controls], SetUnderlinePositionMode method [Windows Controls],ITextFont2 interface, controls.itextfont2_setunderlinepositionmode, tom/ITextFont2::SetUnderlinePositionMode
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
 - ITextFont2.SetUnderlinePositionMode
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::SetUnderlinePositionMode


## -description


Sets the underline position mode.


## -parameters




### -param Value [in]

Type: <b>long</b>

The new underline position mode. It can be one of the following values.<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomUnderlinePositionAuto</a> (the default)</li>
<li><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomUnderlinePositionBelow</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomUnderlinePositionAbove</a></li>
</ul>



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/cd7a45be-05b0-4a43-90c8-0fd8393794c0">ITextFont2::GetUnderlinePositionMode</a>
 

 

