---
UID: NF:tom.ITextDocument.GetDefaultTabStop
title: ITextDocument::GetDefaultTabStop
author: windows-sdk-content
description: Gets the default tab width.
old-location: controls\ITextDocument_GetDefaultTabStop.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getdefaulttabstop.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDefaultTabStop, GetDefaultTabStop method [Windows Controls], GetDefaultTabStop method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],GetDefaultTabStop method, ITextDocument.GetDefaultTabStop, ITextDocument::GetDefaultTabStop, _win32_ITextDocument_GetDefaultTabStop, _win32_ITextDocument_GetDefaultTabStop_cpp, controls.ITextDocument_GetDefaultTabStop, controls._win32_ITextDocument_GetDefaultTabStop, tom/ITextDocument::GetDefaultTabStop
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
 - ITextDocument.GetDefaultTabStop
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument::GetDefaultTabStop


## -description


Gets the default tab width.


## -parameters




### -param pValue

Type: <b>float*</b>

The default tab width. 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If 
						<i>pValue</i> is <b>NULL</b>, the method fails and it returns <b>E_INVALIDARG</b>. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.




## -remarks



The default tab width is used whenever no tab exists beyond the current display position. The default width is given in floating-point points. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787728(v=VS.85).aspx">AddTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787738(v=VS.85).aspx">ClearAllTabs</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787748(v=VS.85).aspx">DeleteTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773989(v=VS.85).aspx">GetListTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774034(v=VS.85).aspx">GetTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774035(v=VS.85).aspx">GetTabCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774052(v=VS.85).aspx">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774177(v=VS.85).aspx">SetListTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

