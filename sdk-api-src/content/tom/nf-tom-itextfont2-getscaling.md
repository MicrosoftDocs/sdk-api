---
UID: NF:tom.ITextFont2.GetScaling
title: ITextFont2::GetScaling
author: windows-sdk-content
description: Gets the font horizontal scaling percentage.
old-location: controls\itextfont2_getscaling.htm
old-project: Controls
ms.assetid: 4508d079-6f75-4842-a7e6-c2b9a99c826c
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetScaling, GetScaling method [Windows Controls], GetScaling method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetScaling method, ITextFont2.GetScaling, ITextFont2::GetScaling, controls.itextfont2_getscaling, tom/ITextFont2::GetScaling
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
 - ITextFont2.GetScaling
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::GetScaling


## -description


Gets the font horizontal scaling percentage.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The scaling percentage.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The font horizontal scaling percentage can range from 200, which doubles the widths of characters, to 0, where no scaling is performed.  When the percentage is increased the height does not change.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/b5f26c0a-a1bd-4be8-84b8-92a6d0cfafdb">ITextFont2::SetScaling</a>
 

 

