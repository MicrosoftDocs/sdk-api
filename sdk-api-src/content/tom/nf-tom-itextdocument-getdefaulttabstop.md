---
UID: NF:tom.ITextDocument.GetDefaultTabStop
title: ITextDocument::GetDefaultTabStop
author: windows-sdk-content
description: Gets the default tab width.
old-location: controls\ITextDocument_GetDefaultTabStop.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getdefaulttabstop.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetDefaultTabStop, GetDefaultTabStop method [Windows Controls], GetDefaultTabStop method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],GetDefaultTabStop method, ITextDocument.GetDefaultTabStop, ITextDocument::GetDefaultTabStop, _win32_ITextDocument_GetDefaultTabStop, _win32_ITextDocument_GetDefaultTabStop_cpp, controls.ITextDocument_GetDefaultTabStop, controls._win32_ITextDocument_GetDefaultTabStop, tom/ITextDocument::GetDefaultTabStop
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
 - ITextDocument.GetDefaultTabStop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/e53d8988-6c0f-405f-b9da-04c83ff0ff64">AddTab</a>



<a href="https://msdn.microsoft.com/61899b21-a883-440d-bb2c-0c65b6ae48c0">ClearAllTabs</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/82950caa-4fbc-4f80-aae4-91feecccef65">DeleteTab</a>



<a href="https://msdn.microsoft.com/1fb072d7-6311-4a44-b1e1-ec6ee9ba654d">GetListTab</a>



<a href="https://msdn.microsoft.com/78e1c637-c2ae-4919-8e2f-8e8b89743ac4">GetTab</a>



<a href="https://msdn.microsoft.com/4440ce51-f504-4489-851f-08895b23a22b">GetTabCount</a>



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/21966279-d84f-4f1a-9e90-5e0e79b14c7e">SetListTab</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

