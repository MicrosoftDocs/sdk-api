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

# PlayEnhMetaFileRecord function


## -description


The <b>PlayEnhMetaFileRecord</b> function plays an enhanced-metafile record by executing the graphics device interface (GDI) functions identified by the record.


## -parameters




### -param hdc [in]

A handle to the device context passed to the <a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a> function.


### -param pht

TBD


### -param pmr

TBD


### -param cht

TBD




#### - lpEnhMetaRecord [in]

A pointer to the enhanced-metafile record to be played.


#### - lpHandletable [in]

A pointer to a table of handles to GDI objects used when playing the metafile. The first entry in this table contains the enhanced-metafile handle.


#### - nHandles [in]

The number of handles in the handle table.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



This is an enhanced-metafile function.

An application typically uses <b>PlayEnhMetaFileRecord</b> in conjunction with the <a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a> function to process and play an enhanced-format metafile one record at a time.

The <i>hdc</i>, <i>lpHandletable</i>, and <i>nHandles</i> parameters must be exactly those passed to the <a href="https://msdn.microsoft.com/c9f04b38-18bc-4b52-8c56-d9475bc30202">EnhMetaFileProc</a> callback procedure by the <a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a> function.

If <b>PlayEnhMetaFileRecord</b> does not recognize a record, it ignores the record and returns <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/51e8937b-0c42-49fe-8930-7af303fce788">PlayEnhMetaFile</a>
 

 

