---
UID: NF:ddeml.DdeCreateDataHandle
title: DdeCreateDataHandle function
author: windows-sdk-content
description: Creates a Dynamic Data Exchange (DDE) object and fills the object with data from the specified buffer. A DDE application uses this function during transactions that involve passing data to the partner application.
old-location: dataxchg\ddecreatedatahandle.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddecreatedatahandle.htm
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DdeCreateDataHandle, DdeCreateDataHandle function [Data Exchange], _win32_DdeCreateDataHandle, _win32_ddecreatedatahandle_cpp, dataxchg.ddecreatedatahandle, ddeml/DdeCreateDataHandle, winui._win32_ddecreatedatahandle
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
api_name:
-	DdeCreateDataHandle
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeCreateDataHandle function


## -description


Creates a Dynamic Data Exchange (DDE) object and fills the object with data from the specified buffer. A DDE application uses this function during transactions that involve passing data to the partner application.


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a> function. 


### -param pSrc [in, optional]

Type: <b>LPBYTE</b>

The data to be copied to the DDE object. If this parameter is <b>NULL</b>, no data is copied to the object. 


### -param cb [in]

Type: <b>DWORD</b>

The amount of memory, in bytes, to copy from the buffer pointed to by 
					<i>pSrc</i>. (include the terminating NULL, if the data is a string). If this parameter is zero, the 
					<i>pSrc</i> parameter is ignored. 


### -param cbOff [in]

Type: <b>DWORD</b>

An offset, in bytes, from the beginning of the buffer pointed to by the 
					<i>pSrc</i> parameter. The data beginning at this offset is copied from the buffer to the DDE object. 


### -param hszItem [in, optional]

Type: <b>HSZ</b>

A handle to the string that specifies the data item corresponding to the DDE object. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a> function. If the data handle is to be used in an <a href="https://msdn.microsoft.com/6001eb7d-59c0-49ec-97ce-26132891188c">XTYP_EXECUTE</a> transaction, this parameter must be 0L. 


### -param wFmt [in]

Type: <b>UINT</b>

The standard clipboard format of the data. 


### -param afCmd [in]

Type: <b>UINT</b>

The creation flags. This parameter can be <b>HDATA_APPOWNED</b>, which specifies that the server application calling the <b>DdeCreateDataHandle</b> function owns the data handle this function creates. This flag enables the application to share the data handle with other DDEML applications rather than creating a separate handle to pass to each application. If this flag is specified, the application must eventually free the shared memory object associated with the handle by using the <a href="https://msdn.microsoft.com/817a6c2a-57e8-4a6d-86db-0c34cfa44999">DdeFreeDataHandle</a> function. If this flag is not specified, the handle becomes invalid in the application that created the handle after the data handle is returned by the application's DDE callback function or is used as a parameter in another DDEML function. 


## -returns



Type: <b>HDDEDATA</b>

If the function succeeds, the return value is a data handle.

If the function fails, the return value is 0L. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



Any unfilled locations in the DDE object are undefined. 

After a data handle has been used as a parameter in another DDEML function or has been returned by a DDE callback function, the handle can be used only for read access to the DDE object identified by the handle. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/7695d435-3bb4-4041-8992-9155efa8911e">DdeAccessData</a>



<a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/817a6c2a-57e8-4a6d-86db-0c34cfa44999">DdeFreeDataHandle</a>



<a href="https://msdn.microsoft.com/26ffce87-b5af-4f5d-9853-1b112e80052f">DdeGetData</a>



<a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

