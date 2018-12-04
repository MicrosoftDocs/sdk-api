---
UID: NF:ddeml.DdeAccessData
title: DdeAccessData function
author: windows-sdk-content
description: Provides access to the data in the specified Dynamic Data Exchange (DDE) object. An application must call the DdeUnaccessData function when it has finished accessing the data in the object.
old-location: dataxchg\ddeaccessdata.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeaccessdata.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DdeAccessData, DdeAccessData function [Data Exchange], _win32_DdeAccessData, _win32_ddeaccessdata_cpp, dataxchg.ddeaccessdata, ddeml/DdeAccessData, winui._win32_ddeaccessdata
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
 - DdeAccessData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

