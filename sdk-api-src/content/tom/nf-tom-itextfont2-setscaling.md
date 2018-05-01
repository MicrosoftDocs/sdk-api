---
UID: NF:tom.ITextFont2.SetScaling
title: ITextFont2::SetScaling method
author: windows-driver-content
description: Sets the font horizontal scaling percentage.
old-location: controls\itextfont2_setscaling.htm
old-project: Controls
ms.assetid: b5f26c0a-a1bd-4be8-84b8-92a6d0cfafdb
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITextFont2, ITextFont2 interface [Windows Controls], SetScaling method, ITextFont2::SetScaling, SetScaling method [Windows Controls], SetScaling method [Windows Controls], ITextFont2 interface, SetScaling,ITextFont2.SetScaling, controls.itextfont2_setscaling, tom/ITextFont2::SetScaling
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextFont2.SetScaling
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::SetScaling method


## -description


Sets the font horizontal scaling percentage.


## -parameters




### -param Value [in]

Type: <b>long</b>

The scaling percentage. Values from 0 through 255 are valid. For example, a value of 200 doubles the widths of characters while retaining the same height. A value of 0 has the same effect as a value of 100; that is, it turns scaling off. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/4508d079-6f75-4842-a7e6-c2b9a99c826c">ITextFont2::GetScaling</a>
 

 

