---
UID: NF:tom.ITextPara.DeleteTab
title: ITextPara::DeleteTab
author: windows-sdk-content
description: Deletes a tab at a specified displacement.
old-location: controls\ITextPara_DeleteTab.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\deletetab.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DeleteTab, DeleteTab method [Windows Controls], DeleteTab method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],DeleteTab method, ITextPara.DeleteTab, ITextPara::DeleteTab, _win32_ITextPara_DeleteTab, _win32_ITextPara_DeleteTab_cpp, controls.ITextPara_DeleteTab, controls._win32_ITextPara_DeleteTab, tom/ITextPara::DeleteTab
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
 - ITextPara.DeleteTab
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara::DeleteTab


## -description


Deletes a tab at a specified displacement. 


## -parameters




### -param tbPos

Type: <b>float</b>

Displacement, in floating-point points, at which a tab should be deleted. 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::DeleteTab</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Value</b></dt>
</dl>
</td>
<td width="60%">
Meaning

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>tbPos</i> value is less than or equal to zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The paragraph format object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787728(v=VS.85).aspx">AddTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787738(v=VS.85).aspx">ClearAllTabs</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb773989(v=VS.85).aspx">GetListTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774034(v=VS.85).aspx">GetTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774035(v=VS.85).aspx">GetTabCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774056(v=VS.85).aspx">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774177(v=VS.85).aspx">SetListTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

