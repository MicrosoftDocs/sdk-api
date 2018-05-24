---
UID: NF:tom.ITextRange.GetDuplicate
title: ITextRange::GetDuplicate
author: windows-driver-content
description: Gets a duplicate of this range object.
old-location: controls\ITextRange_GetDuplicate.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextrange\itextrangegetduplicate.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetDuplicate, GetDuplicate method [Windows Controls], GetDuplicate method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetDuplicate method, ITextRange.GetDuplicate, ITextRange::GetDuplicate, _win32_ITextRange_GetDuplicate, _win32_ITextRange_GetDuplicate_cpp, controls.ITextRange_GetDuplicate, controls._win32_ITextRange_GetDuplicate, tom/ITextRange::GetDuplicate
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
-	ITextRange.GetDuplicate
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::GetDuplicate


## -description


Gets a duplicate of this range object. 


## -parameters




### -param ppRange

Type: <b><a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>**</b>

The duplicate of the range. 


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
ppRange is null.

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
 




## -remarks



To create an insertion point in order to traverse a range, first duplicate the range and then collapse the duplicate at its start character position. Note, a range is characterized by start and end character positions, and the story it belongs to.

Even if the range is actually an <a href="https://msdn.microsoft.com/e6afce18-4f02-4f1c-a2ee-735465d2e168">ITextSelection</a>, the duplicate returned is an <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>. For an example, see the <a href="https://msdn.microsoft.com/e0c95f5b-e147-4c1f-ae1a-def36b0be5c1">ITextRange::FindText</a> method. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e0c95f5b-e147-4c1f-ae1a-def36b0be5c1">FindText</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

