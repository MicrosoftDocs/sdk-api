---
UID: NF:tom.ITextRow.GetCellIndex
title: ITextRow::GetCellIndex
author: windows-driver-content
description: Gets the index of the active cell to get or set parameters for.
old-location: controls\itextrow_getcellindex.htm
old-project: Controls
ms.assetid: 7768e073-929c-43a4-8c4f-a67f89a0e7ee
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetCellIndex, GetCellIndex method [Windows Controls], GetCellIndex method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellIndex method, ITextRow.GetCellIndex, ITextRow::GetCellIndex, controls.itextrow_getcellindex, tom/ITextRow::GetCellIndex
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextRow.GetCellIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRow::GetCellIndex


## -description


Gets the index of the active cell to get or set parameters for.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The cell index.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/4b31ed10-f153-4614-ba96-95271fe4b218">ITextRow::SetCellIndex</a>
 

 

