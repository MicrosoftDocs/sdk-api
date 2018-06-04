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

# DdeAccessData function


## -description


Provides access to the data in the specified Dynamic Data Exchange (DDE) object. An application must call the <a href="https://msdn.microsoft.com/e37e386f-c46e-48ad-a613-a96d8d830652">DdeUnaccessData</a> function when it has finished accessing the data in the object. 


## -parameters




### -param hData [in]

Type: <b>HDDEDATA</b>

A handle to the DDE object to be accessed. 


### -param pcbDataSize [out, optional]

Type: <b>LPDWORD</b>

A pointer to a variable that receives the size, in bytes, of the DDE object identified by the 
					<i>hData</i> parameter. If this parameter is <b>NULL</b>, no size information is returned. 


## -returns



Type: <b>LPBYTE</b>

If the function succeeds, the return value is a pointer to the first byte of data in the DDE object.

If the function fails, the return value is <b>NULL</b>. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



If the 
				<i>hData</i> parameter has not been passed to a Dynamic Data Exchange Management Library (DDEML) function, an application can use the pointer returned by <b>DdeAccessData</b> for read-write access to the DDE object. If 
				<i>hData</i> has already been passed to a DDEML function, the pointer should be used only for read access to the memory object. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/7f8c94b4-7922-41d2-a32a-f5596ff3c39a">DdeAddData</a>



<a href="https://msdn.microsoft.com/4ef31f93-5fb5-400e-9c87-60d99785aae7">DdeCreateDataHandle</a>



<a href="https://msdn.microsoft.com/817a6c2a-57e8-4a6d-86db-0c34cfa44999">DdeFreeDataHandle</a>



<a href="https://msdn.microsoft.com/e37e386f-c46e-48ad-a613-a96d8d830652">DdeUnaccessData</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

