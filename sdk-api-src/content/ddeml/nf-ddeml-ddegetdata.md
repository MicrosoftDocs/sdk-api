---
UID: NF:ddeml.DdeGetData
title: DdeGetData function
author: windows-sdk-content
description: Copies data from the specified Dynamic Data Exchange (DDE) object to the specified local buffer.
old-location: dataxchg\ddegetdata.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddegetdata.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: DdeGetData, DdeGetData function [Data Exchange], _win32_DdeGetData, _win32_ddegetdata_cpp, dataxchg.ddegetdata, ddeml/DdeGetData, winui._win32_ddegetdata
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
 - DdeGetData
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeGetData function


## -description


Copies data from the specified Dynamic Data Exchange (DDE) object to the specified local buffer. 


## -parameters




### -param hData [in]

Type: <b>HDDEDATA</b>

A handle to the DDE object that contains the data to copy. 


### -param pDst [out, optional]

Type: <b>LPBYTE</b>

A pointer to the buffer that receives the data. If this parameter is <b>NULL</b>, the <b>DdeGetData</b> function returns the amount of data, in bytes, that would be copied to the buffer. 


### -param cbMax [in]

Type: <b>DWORD</b>

The maximum amount of data, in bytes, to copy to the buffer pointed to by the 
					<i>pDst</i> parameter. Typically, this parameter specifies the length of the buffer pointed to by 
					<i>pDst</i>. 


### -param cbOff [in]

Type: <b>DWORD</b>

An offset within the DDE object. Data is copied from the object beginning at this offset. 


## -returns



Type: <b>DWORD</b>

If the 
						<i>pDst</i> parameter points to a buffer, the return value is the size, in bytes, of the memory object associated with the data handle or the size specified in the 
						<i>cbMax</i> parameter, whichever is lower. 

If the 
						<i>pDst</i> parameter is <b>NULL</b>, the return value is the size, in bytes, of the memory object associated with the data handle. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/7695d435-3bb4-4041-8992-9155efa8911e">DdeAccessData</a>



<a href="https://msdn.microsoft.com/4ef31f93-5fb5-400e-9c87-60d99785aae7">DdeCreateDataHandle</a>



<a href="https://msdn.microsoft.com/817a6c2a-57e8-4a6d-86db-0c34cfa44999">DdeFreeDataHandle</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

