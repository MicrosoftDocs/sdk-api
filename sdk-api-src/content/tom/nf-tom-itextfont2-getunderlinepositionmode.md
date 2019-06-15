---
UID: NF:tom.ITextFont2.GetUnderlinePositionMode
title: ITextFont2::GetUnderlinePositionMode (tom.h)
author: windows-sdk-content
description: Gets the underline position mode.
old-location: controls\itextfont2_getunderlinepositionmode.htm
tech.root: Controls
ms.assetid: cd7a45be-05b0-4a43-90c8-0fd8393794c0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetUnderlinePositionMode, GetUnderlinePositionMode method [Windows Controls], GetUnderlinePositionMode method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetUnderlinePositionMode method, ITextFont2.GetUnderlinePositionMode, ITextFont2::GetUnderlinePositionMode, controls.itextfont2_getunderlinepositionmode, tom/ITextFont2::GetUnderlinePositionMode
ms.topic: method
f1_keywords: ["tom/ITextFont2.GetUnderlinePositionMode"]
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
 - ITextFont2.GetUnderlinePositionMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextFont2::GetUnderlinePositionMode


## -description


Gets the underline position mode.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The underline position mode. It can be one of the following values.

<a href="https://docs.microsoft.com/windows/desktop/api/tom/ne-tom-__midl___midl_itf_tom_0000_0000_0001">tomUnderlinePositionAuto</a>
<a href="https://docs.microsoft.com/windows/desktop/api/tom/ne-tom-__midl___midl_itf_tom_0000_0000_0001">tomUnderlinePositionBelow</a>
<a href="https://docs.microsoft.com/windows/desktop/api/tom/ne-tom-__midl___midl_itf_tom_0000_0000_0001">tomUnderlinePositionAbove</a>

## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setunderlinepositionmode">ITextFont2::SetUnderlinePositionMode</a>
 

 

