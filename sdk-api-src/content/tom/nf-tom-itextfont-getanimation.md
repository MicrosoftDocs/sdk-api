---
UID: NF:tom.ITextFont.GetAnimation
title: ITextFont::GetAnimation
author: windows-driver-content
description: Gets the animation type.
old-location: controls\ITextFont_GetAnimation.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getanimation.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetAnimation, GetAnimation method [Windows Controls], GetAnimation method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetAnimation method, ITextFont.GetAnimation, ITextFont::GetAnimation, _win32_ITextFont_GetAnimation, _win32_ITextFont_GetAnimation_cpp, controls.ITextFont_GetAnimation, controls._win32_ITextFont_GetAnimation, tom/ITextFont::GetAnimation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
-	ITextFont.GetAnimation
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::GetAnimation


## -description


Gets the animation type.


## -parameters




### -param pValue

Type: <b>long*</b>

One of the following animation types. 
					

<a href="tomconstants.htm">tomNoAnimation</a>
<a href="tomconstants.htm">tomLasVegasLights</a>
<a href="tomconstants.htm">tomBlinkingBackground</a>
<a href="tomconstants.htm">tomSparkleText</a>
<a href="tomconstants.htm">tomMarchingBlackAnts</a>
<a href="tomconstants.htm">tomMarchingRedAnts</a>
<a href="tomconstants.htm">tomShimmer</a>
<a href="tomconstants.htm">tomWipeDown</a>
<a href="tomconstants.htm">tomWipeRight</a>

## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The font object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e3edc0c9-0f75-4b6a-a4c4-b7659bbb89cf">SetAnimation</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

