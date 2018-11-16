---
UID: NF:tom.ITextFont2.SetEffects2
title: ITextFont2::SetEffects2
author: windows-sdk-content
description: Sets the additional character format effects.
old-location: controls\itextfont2_seteffects2.htm
tech.root: Controls
ms.assetid: fb4bfbe3-1e66-41ed-92e6-8d4f3877bdf0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetEffects2 method, ITextFont2.SetEffects2, ITextFont2::SetEffects2, SetEffects2, SetEffects2 method [Windows Controls], SetEffects2 method [Windows Controls],ITextFont2 interface, controls.itextfont2_seteffects2, tom/ITextFont2::SetEffects2, tomAutoSpaceAlpha, tomAutoSpaceNumeric, tomAutoSpaceParens, tomDoublestrike, tomEmbeddedFont, tomModWidthPairs, tomModWidthSpace, tomOverlapping
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
 - ITextFont2.SetEffects2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tom.h
: 
- ITextFont2.SetEffects2
: 
---

# ITextFont2::SetEffects2


## -description


Sets the additional character format effects. 


## -parameters




### -param Value [in]

Type: <b>long</b>

A combination of the following character format flags.

<a id="tomAutoSpaceAlpha"></a>
<a id="tomautospacealpha"></a>
<a id="TOMAUTOSPACEALPHA"></a>


#### tomAutoSpaceAlpha

<a id="tomAutoSpaceNumeric"></a>
<a id="tomautospacenumeric"></a>
<a id="TOMAUTOSPACENUMERIC"></a>


#### tomAutoSpaceNumeric

<a id="tomAutoSpaceParens"></a>
<a id="tomautospaceparens"></a>
<a id="TOMAUTOSPACEPARENS"></a>


#### tomAutoSpaceParens

<a id="tomDoublestrike"></a>
<a id="tomdoublestrike"></a>
<a id="TOMDOUBLESTRIKE"></a>


#### tomDoublestrike

<a id="tomEmbeddedFont"></a>
<a id="tomembeddedfont"></a>
<a id="TOMEMBEDDEDFONT"></a>


#### tomEmbeddedFont

<a id="tomModWidthPairs"></a>
<a id="tommodwidthpairs"></a>
<a id="TOMMODWIDTHPAIRS"></a>


#### tomModWidthPairs

<a id="tomModWidthSpace"></a>
<a id="tommodwidthspace"></a>
<a id="TOMMODWIDTHSPACE"></a>


#### tomModWidthSpace

<a id="tomOverlapping"></a>
<a id="tomoverlapping"></a>
<a id="TOMOVERLAPPING"></a>


#### tomOverlapping


### -param Mask [in]

Type: <b>long</b>

The desired mask, which can be a combination of the <i>Value</i> flags. Only effects with the corresponding mask flag set are modified.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Only effects with the corresponding mask flag set are modified.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/6b28c995-33dd-4f5b-ac89-eec367e0a4d5">ITextFont2::GetEffects2</a>
 

 

