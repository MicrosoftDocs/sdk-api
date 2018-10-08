---
UID: NF:tom.ITextRow.SetCellCountCache
title: ITextRow::SetCellCountCache
author: windows-sdk-content
description: Sets the count of cells cached for a row.
old-location: controls\itextrow_setcellcountcache.htm
tech.root: controls
ms.assetid: 54b9a0a0-1822-4cd6-afef-8ed9403e750a
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellCountCache method, ITextRow.SetCellCountCache, ITextRow::SetCellCountCache, SetCellCountCache, SetCellCountCache method [Windows Controls], SetCellCountCache method [Windows Controls],ITextRow interface, controls.itextrow_setcellcountcache, tom/ITextRow::SetCellCountCache
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
 - ITextRow.SetCellCountCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRow::SetCellCountCache


## -description


Sets the count of cells cached for a row. 


## -parameters




### -param Value [in]

Type: <b>long</b>

The cell count.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If all cells are identical, properties need to be cached only for the cell with index 0. If the cached count is less than the cell count, the cell parameters for index CellCountCache – 1 are used for cells with larger indices.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/e94abbcb-2a7a-4904-a832-0d2158d49010">ITextRow::GetCellCountCache</a>
 

 

