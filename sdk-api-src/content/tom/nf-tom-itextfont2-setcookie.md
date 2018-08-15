---
UID: NF:tom.ITextFont2.SetCookie
title: ITextFont2::SetCookie
author: windows-sdk-content
description: Sets the client cookie.
old-location: controls\itextfont2_setcookie.htm
old-project: controls
ms.assetid: d1b4c7a8-ba4c-482f-8431-14d45474ccc0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetCookie method, ITextFont2.SetCookie, ITextFont2::SetCookie, SetCookie, SetCookie method [Windows Controls], SetCookie method [Windows Controls],ITextFont2 interface, controls.itextfont2_setcookie, tom/ITextFont2::SetCookie
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: 
req.redist: 
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
 - ITextFont2.SetCookie
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::SetCookie


## -description


Sets the client cookie.


## -parameters




### -param Value [in]

Type: <b>long</b>

The client cookie.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This value is purely for the use of the client. It has no meaning to the Text Object Model (TOM) engine except that different values correspond to different character format runs.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/f3e36338-8c88-4aaf-bbd0-c07a2228cb23">ITextFont2::GetCookie</a>
 

 

