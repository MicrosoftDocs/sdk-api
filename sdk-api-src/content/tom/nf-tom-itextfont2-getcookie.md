---
UID: NF:tom.ITextFont2.GetCookie
title: ITextFont2::GetCookie (tom.h)
author: windows-sdk-content
description: Gets the client cookie.
old-location: controls\itextfont2_getcookie.htm
tech.root: Controls
ms.assetid: f3e36338-8c88-4aaf-bbd0-c07a2228cb23
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCookie, GetCookie method [Windows Controls], GetCookie method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetCookie method, ITextFont2.GetCookie, ITextFont2::GetCookie, controls.itextfont2_getcookie, tom/ITextFont2::GetCookie
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
 - ITextFont2.GetCookie
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont2::GetCookie


## -description


Gets the client cookie.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The client cookie.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This value is purely for the use of the client and has no meaning to the Text Object Model (TOM) engine. There are exceptions where different values correspond to different character format runs.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/d1b4c7a8-ba4c-482f-8431-14d45474ccc0">ITextFont2::SetCookie</a>
 

 

