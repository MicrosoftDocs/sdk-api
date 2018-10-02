---
UID: NF:tom.ITextFont.SetAnimation
title: ITextFont::SetAnimation
author: windows-sdk-content
description: Sets the animation type.
old-location: controls\ITextFont_SetAnimation.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setanimation.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ITextFont interface [Windows Controls],SetAnimation method, ITextFont.SetAnimation, ITextFont::SetAnimation, SetAnimation, SetAnimation method [Windows Controls], SetAnimation method [Windows Controls],ITextFont interface, _win32_ITextFont_SetAnimation, _win32_ITextFont_SetAnimation_cpp, controls.ITextFont_SetAnimation, controls._win32_ITextFont_SetAnimation, tom/ITextFont::SetAnimation
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
 - ITextFont.SetAnimation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont::SetAnimation


## -description


Sets the animation type. 


## -parameters




### -param Value [in]

Type: <b>long</b>

The animation type. It can be one of the following values.

<table class="clsStd">
<tr>
<th>Animation type</th>
<th>Value</th>
</tr>
<tr>
<td><b>tomNoAnimation</b></td>
<td>0</td>
</tr>
<tr>
<td><b>tomLasVegasLights</b></td>
<td>1</td>
</tr>
<tr>
<td><b>tomBlinkingBackground</b></td>
<td>2</td>
</tr>
<tr>
<td><b>tomSparkleText</b></td>
<td>3</td>
</tr>
<tr>
<td><b>tomMarchingBlackAnts</b></td>
<td>4</td>
</tr>
<tr>
<td><b>tomMarchingRedAnts</b></td>
<td>5</td>
</tr>
<tr>
<td><b>tomShimmer</b></td>
<td>6</td>
</tr>
<tr>
<td><b>tomWipeDown</b></td>
<td>7</td>
</tr>
<tr>
<td><b>tomWipeRight</b></td>
<td>8</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb773931(v=VS.85).aspx">GetAnimation</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

