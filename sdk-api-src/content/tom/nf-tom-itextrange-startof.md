---
UID: NF:tom.ITextRange.StartOf
title: ITextRange::StartOf
author: windows-sdk-content
description: Moves the range ends to the start of the first overlapping Unit in the range.
old-location: controls\ITextRange_StartOf.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\startof.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextRange interface [Windows Controls],StartOf method, ITextRange.StartOf, ITextRange::StartOf, StartOf, StartOf method [Windows Controls], StartOf method [Windows Controls],ITextRange interface, _win32_ITextRange_StartOf, _win32_ITextRange_StartOf_cpp, controls.ITextRange_StartOf, controls._win32_ITextRange_StartOf, tom/ITextRange::StartOf
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
 - ITextRange.StartOf
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::StartOf


## -description


Moves the range ends to the start of the first overlapping <i>Unit</i> in the range. 


## -parameters




### -param Unit

Type: <b>long</b>

Unit to use in the move operation. For a list of <i>Unit</i> values, see the discussion under <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>. 


### -param Extend

Type: <b>long</b>

How to move the ends of the range. It can be one of the following values.
					

<table class="clsStd">
<tr>
<td>0 (or <b>tomMove</b>)</td>
<td>Collapses a nondegenerate range to the start position by moving the insertion point. This is the default.</td>
</tr>
<tr>
<td>1 (or <b>tomExtend</b>)</td>
<td>Moves the start position to the beginning of the overlapping <i>Unit</i>. Does not move the end position. </td>
</tr>
</table>
 


### -param pDelta

Type: <b>long*</b>

Pointer to a variable that receives the number of characters that the start position is moved. It can be null. On return, <i>pDelta</i> is the signed number of characters that the insertion point or start position is moved. This value is always less than or equal to zero, because the motion is always toward the beginning of the story. 


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Unit is not supported.

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



If the range is an insertion point on a boundary between <i>Unit</i>s, <b>ITextRange::StartOf</b> does not change the start position. 

The <b>ITextRange::StartOf</b> and <a href="https://msdn.microsoft.com/8bee17fc-bbc1-4443-a135-87e76b06467c">ITextRange::EndOf</a> methods differ from the <a href="https://msdn.microsoft.com/19c5de79-59b2-4ae6-bcdc-d525ef479d63">HomeKey</a> and <a href="https://msdn.microsoft.com/f61e82fc-cb38-4263-8142-04283bb195bd">EndKey</a> methods in that the latter extend from the active end, whereas <b>ITextRange::StartOf</b> extends from the start position and <b>ITextRange::EndOf</b> extends from the end position. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f61e82fc-cb38-4263-8142-04283bb195bd">EndKey</a>



<a href="https://msdn.microsoft.com/8bee17fc-bbc1-4443-a135-87e76b06467c">EndOf</a>



<a href="https://msdn.microsoft.com/19c5de79-59b2-4ae6-bcdc-d525ef479d63">HomeKey</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

