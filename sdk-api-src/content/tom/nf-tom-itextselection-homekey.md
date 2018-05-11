---
UID: NF:tom.ITextSelection.HomeKey
title: ITextSelection::HomeKey
author: windows-driver-content
description: Generalizes the functionality of the Home key.
old-location: controls\ITextSelection_HomeKey.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\homekey.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: HomeKey, HomeKey method [Windows Controls], HomeKey method [Windows Controls],ITextSelection interface, ITextSelection interface [Windows Controls],HomeKey method, ITextSelection.HomeKey, ITextSelection::HomeKey, _win32_ITextSelection_HomeKey, _win32_ITextSelection_HomeKey_cpp, controls.ITextSelection_HomeKey, controls._win32_ITextSelection_HomeKey, tom/ITextSelection::HomeKey, tomColumn, tomLine, tomRow, tomStory
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
-	ITextSelection.HomeKey
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextSelection::HomeKey


## -description


Generalizes the functionality of the Home key. 


## -parameters




### -param Unit

Type: <b>long</b>

Unit to use in the Home key operation. It can take on one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomLine"></a><a id="tomline"></a><a id="TOMLINE"></a><dl>
<dt><b>tomLine</b></dt>
</dl>
</td>
<td width="60%">
Depending on 
								<i>Extend</i>, it moves either the insertion point or the active end to the beginning of the first line in the selection. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="tomStory"></a><a id="tomstory"></a><a id="TOMSTORY"></a><dl>
<dt><b>tomStory</b></dt>
</dl>
</td>
<td width="60%">
Depending on 
								<i>Extend</i>, it moves either the insertion point or the active end to the beginning of the first line in the story.

</td>
</tr>
<tr>
<td width="40%"><a id="tomColumn"></a><a id="tomcolumn"></a><a id="TOMCOLUMN"></a><dl>
<dt><b>tomColumn</b></dt>
</dl>
</td>
<td width="60%">
Depending on 
								<i>Extend</i>, it moves either the insertion point or the active end to the beginning of the first column in the selection. This is available only if the TOM engine supports tables.

</td>
</tr>
<tr>
<td width="40%"><a id="tomRow"></a><a id="tomrow"></a><a id="TOMROW"></a><dl>
<dt><b>tomRow</b></dt>
</dl>
</td>
<td width="60%">
Depending on 
								<i>Extend</i>, it moves either the insertion point or the active end to the beginning of the first row in the selection. This is available only if the TOM engine supports tables.

</td>
</tr>
</table>
 


### -param Extend

Type: <b>long</b>

Flag that indicates how to change the selection. If 
					<i>Extend</i> is zero (or <b>tomMove</b>), the method collapses the selection to an insertion point. If 
					<i>Extend</i> is 1 (or <b>tomExtend</b>), the method moves the active end and leaves the other end alone. The default value is zero. 


### -param pDelta

Type: <b>long*</b>

Pointer to a variable that receives the count of characters that the insertion point or the active end is moved. This parameter can be null. 


## -returns



Type: <b>HRESULT</b>

The method returns an 
						<b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
Unit is neither <b>tomLine</b> nor <b>tomStory.</b>

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



The <b>ITextSelection::HomeKey</b> and <a href="https://msdn.microsoft.com/f61e82fc-cb38-4263-8142-04283bb195bd">ITextSelection::EndKey</a> methods are used to mimic the standard Home/End key behavior.

<b>tomLine</b> mimics the Home or End key behavior 
				<i>without</i> the Ctrl key pressed, while <b>tomStory</b> mimics the behavior 
				<i>with</i> the Ctrl key pressed. Similarly, <b>tomMove</b> mimics the Home or End key behavior 
				<i>without</i> the Shift key pressed, while <b>tomExtend</b> mimics the behavior 
				<i>with</i> the Shift key pressed. So 
				<code>HomeKey(tomStory)</code> converts the selection into an insertion point at the beginning of the associated story, while <b>HomeKey</b>(tomStory, tomExtend) moves the active end of the selection to the beginning of the story and leaves the other end where it was.

The <b>HomeKey</b> and 
				<b>EndKey</b> methods are logical methods like the <a href="https://msdn.microsoft.com/e1f22fc3-f8b8-465e-9684-94ddd2875be2">Move</a> methods, rather than directional methods. Thus, they depend on the language that is involved. For example, in Arabic text, <b>HomeKey</b> moves to the right end of a line, whereas in English text, it moves to the left. Thus, <b>HomeKey</b> and 
				<a href="https://msdn.microsoft.com/f61e82fc-cb38-4263-8142-04283bb195bd">EndKey</a> methods are different than the <a href="https://msdn.microsoft.com/d15ee442-708d-4210-925c-f4320d57330a">ITextSelection::MoveLeft</a> and <a href="https://msdn.microsoft.com/7bf0dfad-5397-4898-a794-2789bc5f0291">ITextSelection::MoveRight</a> methods. Also, note that the <b>HomeKey</b> method is quite different from the 
				<b>Start</b> property, which is the cp at the beginning of the selection. <b>HomeKey</b> and 
				<b>EndKey</b> also differ from the <a href="https://msdn.microsoft.com/29e72fbb-525a-478c-a671-74f5940bb973">StartOf</a> and <a href="https://msdn.microsoft.com/8bee17fc-bbc1-4443-a135-87e76b06467c">EndOf</a> methods in that they extend from the active end, whereas 
				<b>StartOf</b> extends from Start and 
				<b>EndOf</b> extends from End.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f61e82fc-cb38-4263-8142-04283bb195bd">EndKey</a>



<a href="https://msdn.microsoft.com/8bee17fc-bbc1-4443-a135-87e76b06467c">EndOf</a>



<a href="https://msdn.microsoft.com/e6afce18-4f02-4f1c-a2ee-735465d2e168">ITextSelection</a>



<a href="https://msdn.microsoft.com/e1f22fc3-f8b8-465e-9684-94ddd2875be2">Move</a>



<a href="https://msdn.microsoft.com/d15ee442-708d-4210-925c-f4320d57330a">MoveLeft</a>



<a href="https://msdn.microsoft.com/7bf0dfad-5397-4898-a794-2789bc5f0291">MoveRight</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/29e72fbb-525a-478c-a671-74f5940bb973">StartOf</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

