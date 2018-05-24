---
UID: NF:tom.ITextPara.GetTabCount
title: ITextPara::GetTabCount
author: windows-driver-content
description: Retrieves the tab count.
old-location: controls\ITextPara_GetTabCount.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\gettabcount.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetTabCount, GetTabCount method [Windows Controls], GetTabCount method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetTabCount method, ITextPara.GetTabCount, ITextPara::GetTabCount, _win32_ITextPara_GetTabCount, _win32_ITextPara_GetTabCount_cpp, controls.ITextPara_GetTabCount, controls._win32_ITextPara_GetTabCount, tom/ITextPara::GetTabCount
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
-	ITextPara.GetTabCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara::GetTabCount


## -description


Retrieves the tab count. 


## -parameters




### -param pCount






#### - pc

Type: <b>long*</b>

The tab count. 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetTabCount</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
The paragraph formatting object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -remarks



The tab count of a new instance can be nonzero, depending on the underlying text engine. For example, Microsoft Word stories begin with no explicit tabs defined, while rich edit instances start with a single explicit tab. To be sure there are no explicit tabs (that is, to set the tab count to zero), call <a href="https://msdn.microsoft.com/61899b21-a883-440d-bb2c-0c65b6ae48c0">ITextPara::ClearAllTabs</a>.




## -see-also




<a href="https://msdn.microsoft.com/e53d8988-6c0f-405f-b9da-04c83ff0ff64">AddTab</a>



<a href="https://msdn.microsoft.com/61899b21-a883-440d-bb2c-0c65b6ae48c0">ClearAllTabs</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/82950caa-4fbc-4f80-aae4-91feecccef65">DeleteTab</a>



<a href="https://msdn.microsoft.com/1fb072d7-6311-4a44-b1e1-ec6ee9ba654d">GetListTab</a>



<a href="https://msdn.microsoft.com/78e1c637-c2ae-4919-8e2f-8e8b89743ac4">GetTab</a>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/21966279-d84f-4f1a-9e90-5e0e79b14c7e">SetListTab</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

