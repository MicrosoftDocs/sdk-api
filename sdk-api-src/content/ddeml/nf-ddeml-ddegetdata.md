---
UID: NF:ddeml.DdeGetData
title: DdeGetData function
author: windows-sdk-content
description: Copies data from the specified Dynamic Data Exchange (DDE) object to the specified local buffer.
old-location: dataxchg\ddegetdata.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddegetdata.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: DdeGetData, DdeGetData function [Data Exchange], _win32_DdeGetData, _win32_ddegetdata_cpp, dataxchg.ddegetdata, ddeml/DdeGetData, winui._win32_ddegetdata
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
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
req.typenames: 
req.redist: 
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

The <a href="https://msdn.microsoft.com/en-us/library/ms648755(v=VS.85).aspx">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648740(v=VS.85).aspx">DdeAccessData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648747(v=VS.85).aspx">DdeCreateDataHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648752(v=VS.85).aspx">DdeFreeDataHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

