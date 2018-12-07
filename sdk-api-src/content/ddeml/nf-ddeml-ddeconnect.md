---
UID: NF:ddeml.DdeConnect
title: DdeConnect function
author: windows-sdk-content
description: Establishes a conversation with a server application that supports the specified service name and topic name pair. If more than one such server exists, the system selects only one.
old-location: dataxchg\ddeconnect.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeconnect.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DdeConnect, DdeConnect function [Data Exchange], _win32_DdeConnect, _win32_ddeconnect_cpp, dataxchg.ddeconnect, ddeml/DdeConnect, winui._win32_ddeconnect
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
 - DdeConnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdeConnect function


## -description


Establishes a conversation with a server application that supports the specified service name and topic name pair. If more than one such server exists, the system selects only one. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a> function. 


### -param hszService [in]

Type: <b>HSZ</b>

A handle to the string that specifies the service name of the server application with which a conversation is to be established. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms648748(v=VS.85).aspx">DdeCreateStringHandle</a> function. If this parameter is 0L, a conversation is established with any available server. 


### -param hszTopic [in]

Type: <b>HSZ</b>

A handle to the string that specifies the name of the topic on which a conversation is to be established. This handle must have been created by a previous call to <a href="https://msdn.microsoft.com/en-us/library/ms648748(v=VS.85).aspx">DdeCreateStringHandle</a>. If this parameter is 0L, a conversation on any topic supported by the selected server is established. 


### -param pCC [in, optional]

Type: <b>PCONVCONTEXT</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms648730(v=VS.85).aspx">CONVCONTEXT</a> structure that contains conversation context information. If this parameter is <b>NULL</b>, the server receives the default <b>CONVCONTEXT</b> structure during the 
					<a href="https://msdn.microsoft.com/en-us/library/ms648718(v=VS.85).aspx">XTYP_CONNECT</a> or 
					<a href="https://msdn.microsoft.com/en-us/library/ms648728(v=VS.85).aspx">XTYP_WILDCONNECT</a> transaction. 
					


## -returns



Type: <b>HCONV</b>

If the function succeeds, the return value is the handle to the established conversation.

If the function fails, the return value is 0L. 

The <a href="https://msdn.microsoft.com/en-us/library/ms648755(v=VS.85).aspx">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



The client application cannot make assumptions regarding the server selected. If an instance-specific name is specified in the 
				<i>hszService</i> parameter, a conversation is established with only the specified instance. Instance-specific service names are passed to an application's Dynamic Data Exchange (DDE) callback function during the <a href="https://msdn.microsoft.com/en-us/library/ms648725(v=VS.85).aspx">XTYP_REGISTER</a> and <a href="https://msdn.microsoft.com/en-us/library/ms648727(v=VS.85).aspx">XTYP_UNREGISTER</a> transactions. 

All members of the default <a href="https://msdn.microsoft.com/en-us/library/ms648730(v=VS.85).aspx">CONVCONTEXT</a> structure are set to zero except 
				<i>cb</i>, which specifies the size of the structure, and 
				<i>iCodePage</i>, which specifies <b>CP_WINANSI</b> (the default code page) or <b>CP_WINUNICODE</b>, depending on whether the ANSI or Unicode version of the <a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a> function was called by the client application. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648730(v=VS.85).aspx">CONVCONTEXT</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648746(v=VS.85).aspx">DdeConnectList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648748(v=VS.85).aspx">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648749(v=VS.85).aspx">DdeDisconnect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648750(v=VS.85).aspx">DdeDisconnectList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648725(v=VS.85).aspx">XTYP_REGISTER</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648727(v=VS.85).aspx">XTYP_UNREGISTER</a>
 

 

