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

# SetMetaFileBitsEx function


## -description


The <b>SetMetaFileBitsEx</b> function creates a memory-based Windows-format metafile from the supplied data.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="https://msdn.microsoft.com/0f21ed97-e37f-4b44-a2eb-b8e284b3dc4b">SetEnhMetaFileBits</a>.</div><div> </div>

## -parameters




### -param cbBuffer

TBD


### -param lpData [in]

Pointer to a buffer that contains the Windows-format metafile. (It is assumed that the data was obtained by using the <a href="https://msdn.microsoft.com/6ca6de2e-79cb-4503-a0d7-f616b8e383eb">GetMetaFileBitsEx</a> function.)


#### - nSize [in]

Specifies the size, in bytes, of the Windows-format metafile.


## -returns



If the function succeeds, the return value is a handle to a memory-based Windows-format metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



To convert a Windows-format metafile into an enhanced-format metafile, use the <a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a> function.

When the application no longer needs the metafile handle returned by <b>SetMetaFileBitsEx</b>, it should delete it by calling the <a href="https://msdn.microsoft.com/51766282-f185-4e29-a36e-1069d9d61f7c">DeleteMetaFile</a> function.




## -see-also




<a href="https://msdn.microsoft.com/51766282-f185-4e29-a36e-1069d9d61f7c">DeleteMetaFile</a>



<a href="https://msdn.microsoft.com/6ca6de2e-79cb-4503-a0d7-f616b8e383eb">GetMetaFileBitsEx</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/0f21ed97-e37f-4b44-a2eb-b8e284b3dc4b">SetEnhMetaFileBits</a>



<a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a>
 

 

