---
UID: NF:faxcomex.IFaxServer.Connect
title: IFaxServer::Connect
author: windows-sdk-content
description: The IFaxServer::Connect method connects a fax client application to the specified fax server.
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_connect_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0ipg.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: Connect, Connect method [Fax Service], Connect method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],Connect method, IFaxServer.Connect, IFaxServer::Connect, _mfax_faxserver.connect, fax._mfax_faxserver_connect, fax._mfax_faxserver_cpp_mfax_faxserver_connect_cpp, faxcomex/IFaxServer::Connect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxServer.Connect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::Connect


## -description


The <b>IFaxServer::Connect</b> method connects a fax client application to the specified fax server.



## -parameters




### -param bstrServerName

Type: <b>BSTR</b>

A null-terminated string that specifies the name of the target fax server, such as "computername". If this parameter is <b>NULL</b> or an empty string, the method connects the application to the fax server on the local computer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before accessing most of the objects of the fax extended Component Object Model (COM), the application must call this method to initiate a connection with an active fax server. A fax server connection is not required for you to access a <a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a> object. The method fails if the client is not connected to an active fax server. 

To connect to the local server, set the <i>bstrServerName</i> parameter to <b>NULL</b> or an empty string. For usage examples, see <a href="https://msdn.microsoft.com/aa3cd5cf-fff5-453b-9574-7ef617239da6">Connecting to the Fax Server</a>.




## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>



<a href="https://msdn.microsoft.com/80437d99-5b9f-4faa-8f09-ed91fc622d4b">Visual Basic Example</a>
 

 

