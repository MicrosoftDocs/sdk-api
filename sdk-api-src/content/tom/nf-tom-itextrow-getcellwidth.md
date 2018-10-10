---
UID: NF:tom.ITextRow.GetCellWidth
title: ITextRow::GetCellWidth
author: windows-sdk-content
description: Gets the width of the active cell.
old-location: controls\itextrow_getcellwidth.htm
tech.root: Controls
ms.assetid: dc73fdf4-29ce-4432-825d-725d61717b7a
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetCellWidth, GetCellWidth method [Windows Controls], GetCellWidth method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellWidth method, ITextRow.GetCellWidth, ITextRow::GetCellWidth, controls.itextrow_getcellwidth, tom/ITextRow::GetCellWidth
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
 - ITextRow.GetCellWidth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRow::GetCellWidth


## -description


Gets the width of the active cell.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The width of the active cell, in twips.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The width of the cell, and/or the entire row, must be less than 22 inches (1440 x 22).




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/321c5255-9cd5-46ea-a592-165d288bc452">ITextRow::SetCellWidth</a>
 

 

