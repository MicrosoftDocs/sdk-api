---
UID: NF:ddeml.DdeAccessData
title: DdeAccessData function
author: windows-sdk-content
description: Provides access to the data in the specified Dynamic Data Exchange (DDE) object. An application must call the DdeUnaccessData function when it has finished accessing the data in the object.
old-location: dataxchg\ddeaccessdata.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeaccessdata.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: DdeAccessData, DdeAccessData function [Data Exchange], _win32_DdeAccessData, _win32_ddeaccessdata_cpp, dataxchg.ddeaccessdata, ddeml/DdeAccessData, winui._win32_ddeaccessdata
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
 - DdeAccessData
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeAccessData function


## -description


Provides access to the data in the specified Dynamic Data Exchange (DDE) object. An application must call the <a href="https://msdn.microsoft.com/library/ms648766(v=VS.85).aspx">DdeUnaccessData</a> function when it has finished accessing the data in the object. 


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

The <a href="https://msdn.microsoft.com/library/ms648755(v=VS.85).aspx">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



If the 
				<i>hData</i> parameter has not been passed to a Dynamic Data Exchange Management Library (DDEML) function, an application can use the pointer returned by <b>DdeAccessData</b> for read-write access to the DDE object. If 
				<i>hData</i> has already been passed to a DDEML function, the pointer should be used only for read access to the memory object. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms648741(v=VS.85).aspx">DdeAddData</a>



<a href="https://msdn.microsoft.com/library/ms648747(v=VS.85).aspx">DdeCreateDataHandle</a>



<a href="https://msdn.microsoft.com/library/ms648752(v=VS.85).aspx">DdeFreeDataHandle</a>



<a href="https://msdn.microsoft.com/library/ms648766(v=VS.85).aspx">DdeUnaccessData</a>



<a href="https://msdn.microsoft.com/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

