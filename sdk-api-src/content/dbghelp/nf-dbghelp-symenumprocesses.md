---
UID: NF:dbghelp.SymEnumProcesses
title: SymEnumProcesses function (dbghelp.h)
author: windows-sdk-content
description: Enumerates each process that has called the SymInitialize function.
old-location: base\symenumprocesses.htm
tech.root: Debug
ms.assetid: 281b83ff-8375-4edb-8a10-97af5dbdc87b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SymEnumProcesses, SymEnumProcesses function, base.symenumprocesses, dbghelp/SymEnumProcesses
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
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
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymEnumProcesses
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
---

# SymEnumProcesses function


## -description


Enumerates each process that has called the <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


## -parameters




### -param EnumProcessesCallback [in]

A <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumprocesses_callback">SymEnumProcessesProc</a> callback function that receives the process information.


### -param UserContext [in]

A user-defined value that is passed to the callback function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context for the callback function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumprocesses_callback">SymEnumProcessesProc</a>
 

 

