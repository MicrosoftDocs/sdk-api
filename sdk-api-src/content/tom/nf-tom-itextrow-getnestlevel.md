---
UID: NF:tom.ITextRow.GetNestLevel
title: ITextRow::GetNestLevel
author: windows-sdk-content
description: Gets the nest level of a table.
old-location: controls\itextrow_getnestlevel.htm
old-project: Controls
ms.assetid: 6b689344-6748-49d7-aa98-a87435b7cb0b
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetNestLevel, GetNestLevel method [Windows Controls], GetNestLevel method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetNestLevel method, ITextRow.GetNestLevel, ITextRow::GetNestLevel, controls.itextrow_getnestlevel, tom/ITextRow::GetNestLevel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: 
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
 - ITextRow.GetNestLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRow::GetNestLevel


## -description


Gets the nest level of a table.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The nest level.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The nest level of the table is identified by the associated <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a> object. If there is only a single table, the nest level is 1. If there is no table, the nest level is 0.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>
 

 

