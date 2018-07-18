---
UID: NF:tom.ITextRange.CanEdit
title: ITextRange::CanEdit
author: windows-sdk-content
description: Determines whether the specified range can be edited.
old-location: controls\ITextRange_CanEdit.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\canedit.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CanEdit, CanEdit method [Windows Controls], CanEdit method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],CanEdit method, ITextRange.CanEdit, ITextRange::CanEdit, _win32_ITextRange_CanEdit, _win32_ITextRange_CanEdit_cpp, controls.ITextRange_CanEdit, controls._win32_ITextRange_CanEdit, tom/ITextRange::CanEdit
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
 - ITextRange.CanEdit
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::CanEdit


## -description


Determines whether the specified range can be edited.


## -parameters




### -param pValue






#### - pbCanEdit [retval]

Type: <b>long*</b>

A <a href="https://msdn.microsoft.com/library/Bb787724(v=VS.85).aspx">tomBool</a> value indicating whether the range can be edited. It is <b>tomTrue</b> only if the specified range can be edited. The pointer can be null.


## -returns



Type: <b>HRESULT</b>

If the range can be edited, the method succeeds and returns <b>S_OK</b>. If the range cannot be edited, the method fails and returns <b>S_FALSE</b>. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.




## -remarks



The range cannot be edited if any part of it is protected or if the document is read-only.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

