---
UID: NF:tom.ITextDocument.SetDefaultTabStop
title: ITextDocument::SetDefaultTabStop
author: windows-sdk-content
description: Sets the default tab stop, which is used when no tab exists beyond the current display position.
old-location: controls\ITextDocument_SetDefaultTabStop.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setdefaulttabstop.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ITextDocument interface [Windows Controls],SetDefaultTabStop method, ITextDocument.SetDefaultTabStop, ITextDocument::SetDefaultTabStop, SetDefaultTabStop, SetDefaultTabStop method [Windows Controls], SetDefaultTabStop method [Windows Controls],ITextDocument interface, _win32_ITextDocument_SetDefaultTabStop, _win32_ITextDocument_SetDefaultTabStop_cpp, controls.ITextDocument_SetDefaultTabStop, controls._win32_ITextDocument_SetDefaultTabStop, tom/ITextDocument::SetDefaultTabStop
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
 - ITextDocument.SetDefaultTabStop
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument::SetDefaultTabStop


## -description


Sets the default tab stop, which is used when no tab exists beyond the current display position. 


## -parameters




### -param Value [in]

Type: <b>float</b>

New default tab setting, in floating-point points. Default value is 36.0 points, that is, 0.5 inches. 


## -returns



Type: <b>HRESULT</b>

If the method succeeds it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e53d8988-6c0f-405f-b9da-04c83ff0ff64">AddTab</a>



<a href="https://msdn.microsoft.com/61899b21-a883-440d-bb2c-0c65b6ae48c0">ClearAllTabs</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/82950caa-4fbc-4f80-aae4-91feecccef65">DeleteTab</a>



<a href="https://msdn.microsoft.com/a7005c4d-3280-4c06-9b23-74e6742f4970">GetDefaultTabStop</a>



<a href="https://msdn.microsoft.com/1fb072d7-6311-4a44-b1e1-ec6ee9ba654d">GetListTab</a>



<a href="https://msdn.microsoft.com/78e1c637-c2ae-4919-8e2f-8e8b89743ac4">GetTab</a>



<a href="https://msdn.microsoft.com/4440ce51-f504-4489-851f-08895b23a22b">GetTabCount</a>



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/21966279-d84f-4f1a-9e90-5e0e79b14c7e">SetListTab</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

