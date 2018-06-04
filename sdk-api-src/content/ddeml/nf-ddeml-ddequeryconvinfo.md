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

# DdeQueryConvInfo function


## -description


Retrieves information about a Dynamic Data Exchange (DDE) transaction and about the conversation in which the transaction takes place. 


## -parameters




### -param hConv [in]

Type: <b>HCONV</b>

A handle to the conversation. 


### -param idTransaction [in]

Type: <b>DWORD</b>

The transaction. For asynchronous transactions, this parameter should be a transaction identifier returned by the <a href="https://msdn.microsoft.com/024655dd-f4de-4aad-a6fe-81e8322e228e">DdeClientTransaction</a> function. For synchronous transactions, this parameter should be QID_SYNC. 


### -param pConvInfo [in, out]

Type: <b>PCONVINFO</b>

A pointer to the <a href="https://msdn.microsoft.com/fb90f16f-d17c-4123-b821-602e8a5d25b1">CONVINFO</a> structure that receives information about the transaction and conversation. The 
					<i>cb</i> member of the <b>CONVINFO</b> structure must specify the length of the buffer allocated for the structure.


## -returns



Type: <b>UINT</b>

If the function succeeds, the return value is the number of bytes copied into the <a href="https://msdn.microsoft.com/fb90f16f-d17c-4123-b821-602e8a5d25b1">CONVINFO</a> structure.

If the function fails, the return value is <b>FALSE</b>. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



An application should not free a string handle referenced by the <a href="https://msdn.microsoft.com/fb90f16f-d17c-4123-b821-602e8a5d25b1">CONVINFO</a> structure. If an application must use one of these string handles, it should call the <a href="https://msdn.microsoft.com/ecef0207-061c-451a-a911-1b821bbe099d">DdeKeepStringHandle</a> function to create a copy of the handle. 

If the 
				<i>idTransaction</i> parameter is set to QID_SYNC, the 
				<i>hUser</i> member of the <a href="https://msdn.microsoft.com/fb90f16f-d17c-4123-b821-602e8a5d25b1">CONVINFO</a> structure is associated with the conversation and can be used to hold data associated with the conversation. If 
				<i>idTransaction</i> is the identifier of an asynchronous transaction, the 
				<i>hUser</i> member is associated only with the current transaction and is valid only for the duration of the transaction. 




## -see-also




<a href="https://msdn.microsoft.com/fb90f16f-d17c-4123-b821-602e8a5d25b1">CONVINFO</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/024655dd-f4de-4aad-a6fe-81e8322e228e">DdeClientTransaction</a>



<a href="https://msdn.microsoft.com/6dfe446f-43e2-4dbc-940b-df9036c5f7aa">DdeConnect</a>



<a href="https://msdn.microsoft.com/26e49ba5-ff60-49cd-84af-f86055d69da0">DdeConnectList</a>



<a href="https://msdn.microsoft.com/ecef0207-061c-451a-a911-1b821bbe099d">DdeKeepStringHandle</a>



<a href="https://msdn.microsoft.com/ffbea772-ab20-4ec7-b25f-04c5487a528d">DdeQueryNextServer</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

