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

# PlayMetaFileRecord function


## -description


The <b>PlayMetaFileRecord</b> function plays a Windows-format metafile record by executing the graphics device interface (GDI) function contained within that record.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="https://msdn.microsoft.com/3eec8c8d-b99f-4500-9d18-b819c097f341">PlayEnhMetaFileRecord</a>.</div><div> </div>

## -parameters




### -param hdc [in]

A handle to a device context.


### -param lpHandleTable

TBD


### -param lpMR

TBD


### -param noObjs

TBD




#### - lpHandletable [in]

A pointer to a <a href="https://msdn.microsoft.com/c0c03c7d-baac-4b59-ba2f-8f6330651b49">HANDLETABLE</a> structure representing the table of handles to GDI objects used when playing the metafile.


#### - lpMetaRecord [in]

A pointer to the Windows-format metafile record.


#### - nHandles [in]

The number of handles in the handle table.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



To convert a Windows-format metafile into an enhanced-format metafile, use the <a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a> function.

An application typically uses <b>PlayMetaFileRecord</b> in conjunction with the <a href="https://msdn.microsoft.com/b11c7467-64a9-442b-8dee-26e15f64a26b">EnumMetaFile</a> function to process and play a Windows-format metafile one record at a time.

The <i>lpHandletable</i> and <i>nHandles</i> parameters must be identical to those passed to the <a href="https://msdn.microsoft.com/ebef5a3f-0dd7-49df-a07d-c55c5e8c868c">EnumMetaFileProc</a> callback procedure by <a href="https://msdn.microsoft.com/b11c7467-64a9-442b-8dee-26e15f64a26b">EnumMetaFile</a>.

If the <b>PlayMetaFileRecord</b> function does not recognize a record, it ignores the record and returns <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/b11c7467-64a9-442b-8dee-26e15f64a26b">EnumMetaFile</a>



<a href="https://msdn.microsoft.com/c0c03c7d-baac-4b59-ba2f-8f6330651b49">HANDLETABLE</a>



<a href="https://msdn.microsoft.com/7c5d6e97-dff1-4c80-a7d3-082413dca469">METARECORD</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/044894df-dc8a-41b2-8810-e0a1b8bc19d8">PlayMetaFile</a>



<a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a>
 

 

