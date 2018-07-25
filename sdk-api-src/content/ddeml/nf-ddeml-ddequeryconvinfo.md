---
UID: NF:ddeml.DdeQueryConvInfo
title: DdeQueryConvInfo function
author: windows-sdk-content
description: Retrieves information about a Dynamic Data Exchange (DDE) transaction and about the conversation in which the transaction takes place.
old-location: dataxchg\ddequeryconvinfo.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddequeryconvinfo.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: DdeQueryConvInfo, DdeQueryConvInfo function [Data Exchange], _win32_DdeQueryConvInfo, _win32_ddequeryconvinfo_cpp, dataxchg.ddequeryconvinfo, ddeml/DdeQueryConvInfo, winui._win32_ddequeryconvinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ddeml.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DDEPOKE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeQueryConvInfo
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
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
 

 

