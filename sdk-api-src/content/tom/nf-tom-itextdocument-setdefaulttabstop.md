---
UID: NF:tom.ITextDocument.SetDefaultTabStop
title: ITextDocument::SetDefaultTabStop
author: windows-sdk-content
description: Sets the default tab stop, which is used when no tab exists beyond the current display position.
old-location: controls\ITextDocument_SetDefaultTabStop.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setdefaulttabstop.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ITextDocument interface [Windows Controls],SetDefaultTabStop method, ITextDocument.SetDefaultTabStop, ITextDocument::SetDefaultTabStop, SetDefaultTabStop, SetDefaultTabStop method [Windows Controls], SetDefaultTabStop method [Windows Controls],ITextDocument interface, _win32_ITextDocument_SetDefaultTabStop, _win32_ITextDocument_SetDefaultTabStop_cpp, controls.ITextDocument_SetDefaultTabStop, controls._win32_ITextDocument_SetDefaultTabStop, tom/ITextDocument::SetDefaultTabStop
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
 - ITextDocument.SetDefaultTabStop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Bb787728(v=VS.85).aspx">AddTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787738(v=VS.85).aspx">ClearAllTabs</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787748(v=VS.85).aspx">DeleteTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773941(v=VS.85).aspx">GetDefaultTabStop</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773989(v=VS.85).aspx">GetListTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774034(v=VS.85).aspx">GetTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774035(v=VS.85).aspx">GetTabCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774052(v=VS.85).aspx">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774177(v=VS.85).aspx">SetListTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

