---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITextRow::GetCellBorderWidths


## -description


Gets the border widths of the active cell.


## -parameters




### -param pduLeft [in]

Type: <b>long*</b>

The active-cell left border width.


### -param pduTop [in]

Type: <b>long*</b>

The active-cell top border width.


### -param pduRight [in]

Type: <b>long*</b>

The active-cell right border width.


### -param pduBottom [in]

Type: <b>long*</b>

The active-cell bottom border width.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/343270e6-8f92-4429-9350-4031ae8bb0e0">ITextRow::SetCellBorderWidths</a>
 

 

