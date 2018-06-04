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

# IRdcFileReader::Read


## -description


The <b>Read</b> method reads the specified amount 
    of data starting at the specified position.


## -parameters




### -param offsetFileStart [in]

Offset from the start of the data at which to start the read.


### -param bytesToRead [in]

Number of bytes to be read.


### -param bytesActuallyRead [out]

Address of a <b>ULONG</b> that will receive the number of bytes read.


### -param buffer [out]

Address of the buffer that receives the data read. This buffer must be at least 
      <i>bytesToRead</i> bytes in size.


### -param eof [out]

Address of a <b>BOOL</b> that is set to <b>TRUE</b> if the end of 
      the file has been read.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Typically RDC will read the file sequentially from start to end. When reading signatures, the file may be read 
    more than once.

If the <b>BOOL</b> pointed to by the <i>eof</i> parameter is not <b>TRUE</b> 
    on return then the value pointed to by the <i>bytesActuallyRead</i> parameter must equal the 
    <i>bytesToRead</i> parameter. If the value pointed to by the <i>eof</i> 
    parameter is set, then the value pointed to by the <i>bytesActuallyRead</i> parameter can be 
    any value between zero and the <i>bytesToRead</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/9684efca-37fd-45ce-a24e-d5276b8ea6af">IRdcFileReader</a>
 

 

