---
UID: NF:ddeml.DdeConnectList
title: DdeConnectList function
author: windows-sdk-content
description: Establishes a conversation with all server applications that support the specified service name and topic name pair.
old-location: dataxchg\ddeconnectlist.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeconnectlist.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DdeConnectList, DdeConnectList function [Data Exchange], _win32_DdeConnectList, _win32_ddeconnectlist_cpp, dataxchg.ddeconnectlist, ddeml/DdeConnectList, winui._win32_ddeconnectlist
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ddeml.h
req.include-header: Windows.h
req.redist: 
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
 - DdeConnectList
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeConnectList function


## -description


Establishes a conversation with all server applications that support the specified service name and topic name pair. An application can also use this function to obtain a list of conversation handles by passing the function an existing conversation handle. The <a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a> removes the handles of any terminated conversations from the conversation list. The resulting conversation list contains the handles of all currently established conversations that support the specified service name and topic name. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a> function. 


### -param hszService [in]

Type: <b>HSZ</b>

A handle to the string that specifies the service name of the server application with which a conversation is to be established. If this parameter is 0L, the system attempts to establish conversations with all available servers that support the specified topic name. 


### -param hszTopic [in]

Type: <b>HSZ</b>

A handle to the string that specifies the name of the topic on which a conversation is to be established. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a> function. If this parameter is 0L, the system will attempt to establish conversations on all topics supported by the selected server (or servers). 


### -param hConvList [in]

Type: <b>HCONVLIST</b>

A handle to the conversation list to be enumerated. This parameter should be 0L if a new conversation list is to be established. 


### -param pCC [in, optional]

Type: <b>PCONVCONTEXT</b>

A pointer to the <a href="https://msdn.microsoft.com/0082c16a-5411-4ed2-a278-cc0f5b136133">CONVCONTEXT</a> structure that contains conversation-context information. If this parameter is <b>NULL</b>, the server receives the default <b>CONVCONTEXT</b> structure during the 
					<a href="https://msdn.microsoft.com/74f43b10-f7ac-4370-9caa-7b9ddf3413ed">XTYP_CONNECT</a> or 
					<a href="https://msdn.microsoft.com/4651e14f-ca13-412e-853d-326a13db78e4">XTYP_WILDCONNECT</a> transaction. 
					


## -returns



Type: <b>HCONVLIST</b>

If the function succeeds, the return value is the handle to a new conversation list.

If the function fails, the return value is 0L. The handle to the old conversation list is no longer valid. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



An application must free the conversation list handle returned by the <b>DdeConnectList</b> function, regardless of whether any conversation handles within the list are active. To free the handle, an application can call <a href="https://msdn.microsoft.com/fd0527ef-116a-445a-b035-2abc161a6719">DdeDisconnectList</a>. 

All members of the default <a href="https://msdn.microsoft.com/0082c16a-5411-4ed2-a278-cc0f5b136133">CONVCONTEXT</a> structure are set to zero except 
				<i>cb</i>, specifying the size of the structure, and 
				<i>iCodePage</i>, specifying <b>CP_WINANSI</b> (the default code page) or <b>CP_WINUNICODE</b>, depending on whether the ANSI or Unicode version of the <a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a> function was called by the client application. 




## -see-also




<a href="https://msdn.microsoft.com/0082c16a-5411-4ed2-a278-cc0f5b136133">CONVCONTEXT</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6dfe446f-43e2-4dbc-940b-df9036c5f7aa">DdeConnect</a>



<a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/e8564954-5abc-4ee1-b246-61fc023c5986">DdeDisconnect</a>



<a href="https://msdn.microsoft.com/fd0527ef-116a-445a-b035-2abc161a6719">DdeDisconnectList</a>



<a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a>



<a href="https://msdn.microsoft.com/ffbea772-ab20-4ec7-b25f-04c5487a528d">DdeQueryNextServer</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

