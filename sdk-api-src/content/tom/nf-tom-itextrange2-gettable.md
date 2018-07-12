---
UID: NF:tom.ITextRange2.GetTable
title: ITextRange2::GetTable
author: windows-sdk-content
description: Gets the table properties in the currently selected table.
old-location: controls\itextrange2_gettable.htm
old-project: controls
ms.assetid: ade77edf-6a9e-4c8d-a522-3158c802b6dd
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: GetTable, GetTable method [Windows Controls], GetTable method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetTable method, ITextRange2.GetTable, ITextRange2::GetTable, controls.itextrange2_gettable, tom/ITextRange2::GetTable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: Tom.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ITextRange2.GetTable
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange2::GetTable


## -description


Not implemented.

Gets the table properties in the currently selected table. 


## -parameters




### -param ppTable [out, retval]

Type: <b>IUnknown**</b>

The table properties.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



To select the table when the insertion point is inside a table, call <a href="https://msdn.microsoft.com/library/Bb787781(v=VS.85).aspx">ITextRange::Expand</a>(tomTable). 

Note: this method isn't implemented in RichEdit (see <a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a> for table functionality).




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

