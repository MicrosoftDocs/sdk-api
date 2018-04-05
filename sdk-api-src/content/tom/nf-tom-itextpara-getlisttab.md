---
UID: NF:tom.ITextPara.GetListTab
title: ITextPara::GetListTab method
author: windows-driver-content
description: Retrieves the list tab setting, which is the distance between the first-line indent and the text on the first line. The numbered or bulleted text is left-justified, centered, or right-justified at the first-line indent value.
old-location: controls\ITextPara_GetListTab.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getlisttab.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: GetListTab method [Windows Controls], GetListTab method [Windows Controls], ITextPara interface, GetListTab,ITextPara.GetListTab, ITextPara, ITextPara interface [Windows Controls], GetListTab method, ITextPara::GetListTab, _win32_ITextPara_GetListTab, _win32_ITextPara_GetListTab_cpp, controls.ITextPara_GetListTab, controls._win32_ITextPara_GetListTab, tom/ITextPara::GetListTab
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
-	ITextPara.GetListTab
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara::GetListTab method


## -description


Retrieves the list tab setting, which is the distance between the first-line indent and the text on the first line. The numbered or bulleted text is left-justified, centered, or right-justified at the first-line indent value. 


## -parameters




### -param pValue

Type: <b>float*</b>

The list tab setting. The list tab value is in floating-point points. 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetListTab</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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



To determine whether the numbered or bulleted text is left-justified, centered, or right-justified, call <a href="https://msdn.microsoft.com/bc6785be-4e05-48fb-97ae-6f3e3518db9f">ITextPara::GetListAlignment</a>.




## -see-also




<a href="https://msdn.microsoft.com/e53d8988-6c0f-405f-b9da-04c83ff0ff64">AddTab</a>



<a href="https://msdn.microsoft.com/61899b21-a883-440d-bb2c-0c65b6ae48c0">ClearAllTabs</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/82950caa-4fbc-4f80-aae4-91feecccef65">DeleteTab</a>



<a href="https://msdn.microsoft.com/82831ef0-7ece-4d85-96f5-aa3c4591e458">GetFirstLineIndent</a>



<a href="https://msdn.microsoft.com/bc6785be-4e05-48fb-97ae-6f3e3518db9f">GetListAlignment</a>



<a href="https://msdn.microsoft.com/78e1c637-c2ae-4919-8e2f-8e8b89743ac4">GetTab</a>



<a href="https://msdn.microsoft.com/4440ce51-f504-4489-851f-08895b23a22b">GetTabCount</a>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/21966279-d84f-4f1a-9e90-5e0e79b14c7e">SetListTab</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

