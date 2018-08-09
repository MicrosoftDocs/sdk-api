---
UID: NF:ddeml.DdeUnaccessData
title: DdeUnaccessData function
author: windows-sdk-content
description: Unaccesses a Dynamic Data Exchange (DDE) object. An application must call this function after it has finished accessing the object.
old-location: dataxchg\ddeunaccessdata.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeunaccessdata.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DdeUnaccessData, DdeUnaccessData function [Data Exchange], _win32_DdeUnaccessData, _win32_ddeunaccessdata_cpp, dataxchg.ddeunaccessdata, ddeml/DdeUnaccessData, winui._win32_ddeunaccessdata
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
 - DdeUnaccessData
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

The <a href="https://msdn.microsoft.com/en-us/library/ms648755(v=VS.85).aspx">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648740(v=VS.85).aspx">DdeAccessData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648741(v=VS.85).aspx">DdeAddData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648747(v=VS.85).aspx">DdeCreateDataHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648752(v=VS.85).aspx">DdeFreeDataHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

