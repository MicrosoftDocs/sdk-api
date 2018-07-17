---
UID: NF:tom.ITextRange.GetPoint
title: ITextRange::GetPoint
author: windows-sdk-content
description: Retrieves screen coordinates for the start or end character position in the text range, along with the intra-line position.
old-location: controls\ITextRange_GetPoint.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getpoint.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetPoint, GetPoint method [Windows Controls], GetPoint method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetPoint method, ITextRange.GetPoint, ITextRange::GetPoint, _win32_ITextRange_GetPoint, _win32_ITextRange_GetPoint_cpp, controls.ITextRange_GetPoint, controls._win32_ITextRange_GetPoint, tom/ITextRange::GetPoint, tomAllowOffClient, tomClientCoord, tomEnd, tomObjectArg, tomStart, tomTransform
ms.prod: windows
ms.technology: windows-sdk
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
 - ITextRange.GetPoint
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::GetPoint


## -description


Retrieves screen coordinates for the start or end character position in the text range, along with the intra-line position.


## -parameters




### -param Type

Type: <b>long</b>

Flag that indicates the position to retrieve. This parameter can include one value from each of the following tables. The default value is tomStart + TA_BASELINE + TA_LEFT.

<a id="tomAllowOffClient"></a>
<a id="tomallowoffclient"></a>
<a id="TOMALLOWOFFCLIENT"></a>


#### tomAllowOffClient

<a id="tomClientCoord"></a>
<a id="tomclientcoord"></a>
<a id="TOMCLIENTCOORD"></a>


#### tomClientCoord

<a id="tomObjectArg"></a>
<a id="tomobjectarg"></a>
<a id="TOMOBJECTARG"></a>


#### tomObjectArg

<a id="tomTransform"></a>
<a id="tomtransform"></a>
<a id="TOMTRANSFORM"></a>


#### tomTransform

Use one of the following values to indicate the start or end of the range. 
					

<a id="tomStart"></a>
<a id="tomstart"></a>
<a id="TOMSTART"></a>


#### tomStart

<a id="tomEnd"></a>
<a id="tomend"></a>
<a id="TOMEND"></a>


#### tomEnd

Use one of the following values to indicate the vertical position. 
						<table class="clsStd">
<tr>
<td>TA_TOP</td>
<td>Top edge of the bounding rectangle.</td>
</tr>
<tr>
<td>TA_BASELINE</td>
<td>Base line of the text.</td>
</tr>
<tr>
<td>TA_BOTTOM</td>
<td>Bottom edge of the bounding rectangle.</td>
</tr>
</table>
 



Use one of the following values to indicate the horizontal position. 
						<table class="clsStd">
<tr>
<td>TA_LEFT</td>
<td>Left edge of the bounding rectangle.</td>
</tr>
<tr>
<td>TA_CENTER</td>
<td>Center of the bounding rectangle.</td>
</tr>
<tr>
<td>TA_RIGHT</td>
<td>Right edge of the bounding rectangle.</td>
</tr>
</table>
 




### -param px

Type: <b>long*</b>

The x-coordinate. 


### -param py

Type: <b>long*</b>

The y-coordinate. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
Either <i>px</i> or <i>py</i> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>
 




## -remarks



The <b>ITextRange::GetPoint</b> method gives <a href="https://msdn.microsoft.com/library/Bb774058(v=VS.85).aspx">ITextRange</a> the ability to emulate UI-pointer commands; it is also handy for accessibility purposes. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb787799(v=VS.85).aspx">SetPoint</a>



<a href="https://msdn.microsoft.com/422868c5-14c9-4374-9cc5-b7bf91ab9eb4">SetTextAlign</a>



<a href="https://msdn.microsoft.com/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

