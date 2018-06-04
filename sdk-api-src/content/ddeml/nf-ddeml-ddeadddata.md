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

# DdeAddData function


## -description


Adds data to the specified Dynamic Data Exchange (DDE) object. An application can add data starting at any offset from the beginning of the object. If new data overlaps data already in the object, the new data overwrites the old data in the bytes where the overlap occurs. The contents of locations in the object that have not been written to are undefined. 


## -parameters




### -param hData [in]

Type: <b>HDDEDATA</b>

A handle to the DDE object that receives additional data. 


### -param pSrc [in]

Type: <b>LPBYTE</b>

The data to be added to the DDE object. 


### -param cb [in]

Type: <b>DWORD</b>

The length, in bytes, of the data to be added to the DDE object, including the terminating <b>NULL</b>, if the data is a string. 


### -param cbOff [in]

Type: <b>DWORD</b>

An offset, in bytes, from the beginning of the DDE object. The additional data is copied to the object beginning at this offset. 


## -returns



Type: <b>HDDEDATA</b>

If the function succeeds, the return value is a new handle to the DDE object. The new handle is used in all references to the object. 

If the function fails, the return value is zero. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:




## -remarks



After a data handle has been used as a parameter in another <a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a> function or has been returned by a DDE callback function, the handle can be used only for read access to the DDE object identified by the handle. 

If the amount of memory originally allocated is less than is needed to hold the added data, <b>DdeAddData</b> reallocates a global memory object of the appropriate size. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/7695d435-3bb4-4041-8992-9155efa8911e">DdeAccessData</a>



<a href="https://msdn.microsoft.com/4ef31f93-5fb5-400e-9c87-60d99785aae7">DdeCreateDataHandle</a>



<a href="https://msdn.microsoft.com/e37e386f-c46e-48ad-a613-a96d8d830652">DdeUnaccessData</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

