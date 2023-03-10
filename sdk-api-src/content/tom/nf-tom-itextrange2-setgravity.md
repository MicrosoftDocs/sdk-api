---
UID: NF:tom.ITextRange2.SetGravity
title: ITextRange2::SetGravity (tom.h)
description: Sets the gravity of this range.
helpviewer_keywords: ["ITextRange2 interface [Windows Controls]","SetGravity method","ITextRange2.SetGravity","ITextRange2::SetGravity","SetGravity","SetGravity method [Windows Controls]","SetGravity method [Windows Controls]","ITextRange2 interface","controls.itextrange2_setgravity","tom/ITextRange2::SetGravity","tomGravityBack","tomGravityFore","tomGravityIn","tomGravityOut","tomGravityUI"]
old-location: controls\itextrange2_setgravity.htm
tech.root: Controls
ms.assetid: 10214543-36da-46e3-b926-0ba088f84a7b
ms.date: 12/05/2018
ms.keywords: ITextRange2 interface [Windows Controls],SetGravity method, ITextRange2.SetGravity, ITextRange2::SetGravity, SetGravity, SetGravity method [Windows Controls], SetGravity method [Windows Controls],ITextRange2 interface, controls.itextrange2_setgravity, tom/ITextRange2::SetGravity, tomGravityBack, tomGravityFore, tomGravityIn, tomGravityOut, tomGravityUI
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
 - ITextRange2::SetGravity
 - tom/ITextRange2::SetGravity
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
 - ITextRange2.SetGravity
---

# ITextRange2::SetGravity


## -description

Sets the gravity of this range.

## -parameters

### -param Value [in]

Type: <b>long</b>

The new gravity value, which can be one of the following.

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



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-getgravity">ITextRange2::GetGravity</a>