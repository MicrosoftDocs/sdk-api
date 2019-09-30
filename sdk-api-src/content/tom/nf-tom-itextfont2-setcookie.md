---
UID: NF:tom.ITextFont2.SetCookie
title: ITextFont2::SetCookie (tom.h)
author: windows-sdk-content
description: Sets the client cookie.
old-location: controls\itextfont2_setcookie.htm
tech.root: Controls
ms.assetid: d1b4c7a8-ba4c-482f-8431-14d45474ccc0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetCookie method, ITextFont2.SetCookie, ITextFont2::SetCookie, SetCookie, SetCookie method [Windows Controls], SetCookie method [Windows Controls],ITextFont2 interface, controls.itextfont2_setcookie, tom/ITextFont2::SetCookie
ms.topic: method
f1_keywords: 
 - "tom/ITextFont2.SetCookie"
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
 - ITextFont2.SetCookie
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextFont2::SetCookie


## -description


Sets the client cookie.


## -parameters




### -param Value [in]

Type: <b>long</b>

The client cookie.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This value is purely for the use of the client. It has no meaning to the Text Object Model (TOM) engine except that different values correspond to different character format runs.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getcookie">ITextFont2::GetCookie</a>
 

 

