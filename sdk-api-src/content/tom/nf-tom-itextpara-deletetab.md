---
UID: NF:tom.ITextPara.DeleteTab
title: ITextPara::DeleteTab
author: windows-sdk-content
description: Deletes a tab at a specified displacement.
old-location: controls\ITextPara_DeleteTab.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\deletetab.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DeleteTab, DeleteTab method [Windows Controls], DeleteTab method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],DeleteTab method, ITextPara.DeleteTab, ITextPara::DeleteTab, _win32_ITextPara_DeleteTab, _win32_ITextPara_DeleteTab_cpp, controls.ITextPara_DeleteTab, controls._win32_ITextPara_DeleteTab, tom/ITextPara::DeleteTab
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
 - ITextPara.DeleteTab
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/e53d8988-6c0f-405f-b9da-04c83ff0ff64">AddTab</a>



<a href="https://msdn.microsoft.com/61899b21-a883-440d-bb2c-0c65b6ae48c0">ClearAllTabs</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1fb072d7-6311-4a44-b1e1-ec6ee9ba654d">GetListTab</a>



<a href="https://msdn.microsoft.com/78e1c637-c2ae-4919-8e2f-8e8b89743ac4">GetTab</a>



<a href="https://msdn.microsoft.com/4440ce51-f504-4489-851f-08895b23a22b">GetTabCount</a>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/21966279-d84f-4f1a-9e90-5e0e79b14c7e">SetListTab</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

