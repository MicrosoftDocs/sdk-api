---
UID: NF:tom.ITextRange.GetPara
title: ITextRange::GetPara
author: windows-sdk-content
description: Gets an ITextPara object with the paragraph attributes of the specified range.
old-location: controls\ITextRange_GetPara.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getpara.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetPara, GetPara method [Windows Controls], GetPara method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetPara method, ITextRange.GetPara, ITextRange::GetPara, _win32_ITextRange_GetPara, _win32_ITextRange_GetPara_cpp, controls.ITextRange_GetPara, controls._win32_ITextRange_GetPara, tom/ITextRange::GetPara
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
 - ITextRange.GetPara
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::GetPara


## -description


Gets an <a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a> object with the paragraph attributes of the specified range.


## -parameters




### -param ppPara

Type: <b><a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>**</b>

The pointer to the <a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a> object. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>ppPara</i> is null, the method fails and it returns E_INVALIDARG.




## -remarks



For plain-text controls, these objects do not vary from range to range, but in rich-text solutions, they do. See the section on <a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a> for further details.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

