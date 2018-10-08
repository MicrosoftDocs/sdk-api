---
UID: NF:tom.ITextStoryRanges.Item
title: ITextStoryRanges::Item
author: windows-sdk-content
description: Retrieves an ITextRange object for the Indexth story in this story collection.
old-location: controls\ITextStoryRanges_Item.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\item.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ITextStoryRanges interface [Windows Controls],Item method, ITextStoryRanges.Item, ITextStoryRanges::Item, Item, Item method [Windows Controls], Item method [Windows Controls],ITextStoryRanges interface, _win32_ITextStoryRanges_Item, _win32_ITextStoryRanges_Item_cpp, controls.ITextStoryRanges_Item, controls._win32_ITextStoryRanges_Item, tom/ITextStoryRanges::Item
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
 - ITextStoryRanges.Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStoryRanges::Item


## -description


Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a> object for the 
			<i>Index</i>th story in this story collection. 


## -parameters




### -param Index

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Index of story range that is retrieved. The default value is 1, which indicates the first story in the collection. <i>Count</i>, given by <a href="https://msdn.microsoft.com/en-us/library/Bb773939(v=VS.85).aspx">ITextStoryRanges::GetCount</a>, indicates the last story in the collection. If <i>Index</i> is less than zero, the stories are counted from last to first, with -1 being the index of the last story in the collection, and 
					<i>Index</i> = - <i>Count</i> indicating the first story in the collection. 


### -param ppRange

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>**</b>

The <a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a> object.


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
ppRange is null or Index is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb773939(v=VS.85).aspx">GetCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774062(v=VS.85).aspx">ITextStoryRanges</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

