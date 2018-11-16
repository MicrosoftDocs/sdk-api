---
UID: NF:ddeml.DdeDisconnectList
title: DdeDisconnectList function
author: windows-sdk-content
description: Destroys the specified conversation list and terminates all conversations associated with the list.
old-location: dataxchg\ddedisconnectlist.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddedisconnectlist.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DdeDisconnectList, DdeDisconnectList function [Data Exchange], _win32_DdeDisconnectList, _win32_ddedisconnectlist_cpp, dataxchg.ddedisconnectlist, ddeml/DdeDisconnectList, winui._win32_ddedisconnectlist
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
 - DdeDisconnectList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DdeDisconnectList
: 
---

# DdeDisconnectList function


## -description


Destroys the specified conversation list and terminates all conversations associated with the list. 


## -parameters




### -param hConvList [in]

Type: <b>HCONVLIST</b>

A handle to the conversation list. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms648746(v=VS.85).aspx">DdeConnectList</a> function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="https://msdn.microsoft.com/en-us/library/ms648755(v=VS.85).aspx">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



An application can use the <a href="https://msdn.microsoft.com/en-us/library/ms648749(v=VS.85).aspx">DdeDisconnect</a> function to terminate individual conversations in the list. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648745(v=VS.85).aspx">DdeConnect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648746(v=VS.85).aspx">DdeConnectList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648749(v=VS.85).aspx">DdeDisconnect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

