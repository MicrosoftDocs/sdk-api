---
UID: NF:tom.ITextRange2.GetGravity
title: ITextRange2::GetGravity (tom.h)
description: Gets the gravity of this range.
helpviewer_keywords: ["GetGravity","GetGravity method [Windows Controls]","GetGravity method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetGravity method","ITextRange2.GetGravity","ITextRange2::GetGravity","controls.itextrange2_getgravity","tom/ITextRange2::GetGravity","tomGravityBack","tomGravityFore","tomGravityIn","tomGravityOut","tomGravityUI"]
old-location: controls\itextrange2_getgravity.htm
tech.root: Controls
ms.assetid: a57ab2c2-1871-413a-bccd-47f5c1dd4570
ms.date: 12/05/2018
ms.keywords: GetGravity, GetGravity method [Windows Controls], GetGravity method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetGravity method, ITextRange2.GetGravity, ITextRange2::GetGravity, controls.itextrange2_getgravity, tom/ITextRange2::GetGravity, tomGravityBack, tomGravityFore, tomGravityIn, tomGravityOut, tomGravityUI
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextRange2::GetGravity
 - tom/ITextRange2::GetGravity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange2.GetGravity
---

# ITextRange2::GetGravity


## -description

Gets the gravity of this range.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The gravity value, which can be one of the following: 

<a id="tomGravityUI"></a>
<a id="tomgravityui"></a>
<a id="TOMGRAVITYUI"></a>


#### tomGravityUI

<a id="tomGravityBack"></a>
<a id="tomgravityback"></a>
<a id="TOMGRAVITYBACK"></a>


#### tomGravityBack

<a id="tomGravityFore"></a>
<a id="tomgravityfore"></a>
<a id="TOMGRAVITYFORE"></a>


#### tomGravityFore

<a id="tomGravityIn"></a>
<a id="tomgravityin"></a>
<a id="TOMGRAVITYIN"></a>


#### tomGravityIn

<a id="tomGravityOut"></a>
<a id="tomgravityout"></a>
<a id="TOMGRAVITYOUT"></a>


#### tomGravityOut

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-setgravity">ITextRange2::SetGravity</a>