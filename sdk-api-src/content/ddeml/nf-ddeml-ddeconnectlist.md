---
UID: NF:ddeml.DdeConnectList
title: DdeConnectList function
author: windows-sdk-content
description: Establishes a conversation with all server applications that support the specified service name and topic name pair.
old-location: dataxchg\ddeconnectlist.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeconnectlist.htm
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: DdeConnectList, DdeConnectList function [Data Exchange], _win32_DdeConnectList, _win32_ddeconnectlist_cpp, dataxchg.ddeconnectlist, ddeml/DdeConnectList, winui._win32_ddeconnectlist
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
 - DdeConnectList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DdeConnectList
: 
---

# DdeConnectList function


## -description


Establishes a conversation with all server applications that support the specified service name and topic name pair. An application can also use this function to obtain a list of conversation handles by passing the function an existing conversation handle. The <a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a> removes the handles of any terminated conversations from the conversation list. The resulting conversation list contains the handles of all currently established conversations that support the specified service name and topic name. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a> function. 


### -param hszService [in]

Type: <b>HSZ</b>

A handle to the string that specifies the service name of the server application with which a conversation is to be established. If this parameter is 0L, the system attempts to establish conversations with all available servers that support the specified topic name. 


### -param hszTopic [in]

Type: <b>HSZ</b>

A handle to the string that specifies the name of the topic on which a conversation is to be established. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms648748(v=VS.85).aspx">DdeCreateStringHandle</a> function. If this parameter is 0L, the system will attempt to establish conversations on all topics supported by the selected server (or servers). 


### -param hConvList [in]

Type: <b>HCONVLIST</b>

A handle to the conversation list to be enumerated. This parameter should be 0L if a new conversation list is to be established. 


### -param pCC [in, optional]

Type: <b>PCONVCONTEXT</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms648730(v=VS.85).aspx">CONVCONTEXT</a> structure that contains conversation-context information. If this parameter is <b>NULL</b>, the server receives the default <b>CONVCONTEXT</b> structure during the 
					<a href="https://msdn.microsoft.com/en-us/library/ms648718(v=VS.85).aspx">XTYP_CONNECT</a> or 
					<a href="https://msdn.microsoft.com/en-us/library/ms648728(v=VS.85).aspx">XTYP_WILDCONNECT</a> transaction. 
					


## -returns



Type: <b>HCONVLIST</b>

If the function succeeds, the return value is the handle to a new conversation list.

If the function fails, the return value is 0L. The handle to the old conversation list is no longer valid. 

The <a href="https://msdn.microsoft.com/en-us/library/ms648755(v=VS.85).aspx">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



An application must free the conversation list handle returned by the <b>DdeConnectList</b> function, regardless of whether any conversation handles within the list are active. To free the handle, an application can call <a href="https://msdn.microsoft.com/en-us/library/ms648750(v=VS.85).aspx">DdeDisconnectList</a>. 

All members of the default <a href="https://msdn.microsoft.com/en-us/library/ms648730(v=VS.85).aspx">CONVCONTEXT</a> structure are set to zero except 
				<i>cb</i>, specifying the size of the structure, and 
				<i>iCodePage</i>, specifying <b>CP_WINANSI</b> (the default code page) or <b>CP_WINUNICODE</b>, depending on whether the ANSI or Unicode version of the <a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a> function was called by the client application. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648730(v=VS.85).aspx">CONVCONTEXT</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648745(v=VS.85).aspx">DdeConnect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648748(v=VS.85).aspx">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648749(v=VS.85).aspx">DdeDisconnect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648750(v=VS.85).aspx">DdeDisconnectList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648762(v=VS.85).aspx">DdeQueryNextServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

