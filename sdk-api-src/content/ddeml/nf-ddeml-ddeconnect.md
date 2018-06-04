---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DdeConnect function


## -description


Establishes a conversation with a server application that supports the specified service name and topic name pair. If more than one such server exists, the system selects only one. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a> function. 


### -param hszService [in]

Type: <b>HSZ</b>

A handle to the string that specifies the service name of the server application with which a conversation is to be established. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a> function. If this parameter is 0L, a conversation is established with any available server. 


### -param hszTopic [in]

Type: <b>HSZ</b>

A handle to the string that specifies the name of the topic on which a conversation is to be established. This handle must have been created by a previous call to <a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a>. If this parameter is 0L, a conversation on any topic supported by the selected server is established. 


### -param pCC [in, optional]

Type: <b>PCONVCONTEXT</b>

A pointer to the <a href="https://msdn.microsoft.com/0082c16a-5411-4ed2-a278-cc0f5b136133">CONVCONTEXT</a> structure that contains conversation context information. If this parameter is <b>NULL</b>, the server receives the default <b>CONVCONTEXT</b> structure during the 
					<a href="https://msdn.microsoft.com/74f43b10-f7ac-4370-9caa-7b9ddf3413ed">XTYP_CONNECT</a> or 
					<a href="https://msdn.microsoft.com/4651e14f-ca13-412e-853d-326a13db78e4">XTYP_WILDCONNECT</a> transaction. 
					


## -returns



Type: <b>HCONV</b>

If the function succeeds, the return value is the handle to the established conversation.

If the function fails, the return value is 0L. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



The client application cannot make assumptions regarding the server selected. If an instance-specific name is specified in the 
				<i>hszService</i> parameter, a conversation is established with only the specified instance. Instance-specific service names are passed to an application's Dynamic Data Exchange (DDE) callback function during the <a href="https://msdn.microsoft.com/465e9c10-1526-4e2a-8a46-5984043f5a93">XTYP_REGISTER</a> and <a href="https://msdn.microsoft.com/a57a5d53-7919-4698-8c84-6142dd29bb2a">XTYP_UNREGISTER</a> transactions. 

All members of the default <a href="https://msdn.microsoft.com/0082c16a-5411-4ed2-a278-cc0f5b136133">CONVCONTEXT</a> structure are set to zero except 
				<i>cb</i>, which specifies the size of the structure, and 
				<i>iCodePage</i>, which specifies <b>CP_WINANSI</b> (the default code page) or <b>CP_WINUNICODE</b>, depending on whether the ANSI or Unicode version of the <a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a> function was called by the client application. 




## -see-also




<a href="https://msdn.microsoft.com/0082c16a-5411-4ed2-a278-cc0f5b136133">CONVCONTEXT</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/26e49ba5-ff60-49cd-84af-f86055d69da0">DdeConnectList</a>



<a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/e8564954-5abc-4ee1-b246-61fc023c5986">DdeDisconnect</a>



<a href="https://msdn.microsoft.com/fd0527ef-116a-445a-b035-2abc161a6719">DdeDisconnectList</a>



<a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/465e9c10-1526-4e2a-8a46-5984043f5a93">XTYP_REGISTER</a>



<a href="https://msdn.microsoft.com/a57a5d53-7919-4698-8c84-6142dd29bb2a">XTYP_UNREGISTER</a>
 

 

