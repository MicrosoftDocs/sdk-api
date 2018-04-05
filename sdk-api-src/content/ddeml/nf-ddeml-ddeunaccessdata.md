---
UID: NF:ddeml.DdeUnaccessData
title: DdeUnaccessData function
author: windows-driver-content
description: Unaccesses a Dynamic Data Exchange (DDE) object. An application must call this function after it has finished accessing the object.
old-location: dataxchg\ddeunaccessdata.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeunaccessdata.htm
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: DdeUnaccessData, DdeUnaccessData function [Data Exchange], _win32_DdeUnaccessData, _win32_ddeunaccessdata_cpp, dataxchg.ddeunaccessdata, ddeml/DdeUnaccessData, winui._win32_ddeunaccessdata
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
req.typenames: DDEPOKE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
api_name:
-	DdeUnaccessData
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeUnaccessData function


## -description


Unaccesses a Dynamic Data Exchange (DDE) object. An application must call this function after it has finished accessing the object. 


## -parameters




### -param hData [in]

Type: <b>HDDEDATA</b>

A handle to the DDE object. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/7695d435-3bb4-4041-8992-9155efa8911e">DdeAccessData</a>



<a href="https://msdn.microsoft.com/7f8c94b4-7922-41d2-a32a-f5596ff3c39a">DdeAddData</a>



<a href="https://msdn.microsoft.com/4ef31f93-5fb5-400e-9c87-60d99785aae7">DdeCreateDataHandle</a>



<a href="https://msdn.microsoft.com/817a6c2a-57e8-4a6d-86db-0c34cfa44999">DdeFreeDataHandle</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

