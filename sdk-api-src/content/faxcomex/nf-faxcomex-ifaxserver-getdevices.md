---
UID: NF:faxcomex.IFaxServer.GetDevices
title: IFaxServer::GetDevices
author: windows-sdk-content
description: The GetDevices method creates a FaxDevices object, a collection of all the fax devices exposed by all the fax service providers (FSPs) currently registered with the fax service.
old-location: fax\_mfax_faxserver_getdevices.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7hrn.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FaxServer object [Fax Service],GetDevices method, FaxServer.GetDevices, GetDevices, GetDevices method [Fax Service], GetDevices method [Fax Service],FaxServer object, IFaxServer.GetDevices, IFaxServer::GetDevices, _mfax_faxserver.getdevices, fax._mfax_faxserver_getdevices
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxServer.GetDevices
 - IFaxServer.GetDevices
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxServer::GetDevices


## -description


The <b>GetDevices</b> method creates a <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> object, a collection of all the fax devices exposed by all the fax service providers (FSPs) currently registered with the fax service.


## -parameters




### -param ppFaxDevices






## -returns



Type: <b><a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a>**</b>

A <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> object.




## -remarks



You can use the <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> object to enumerate the fax devices associated with a connected fax server and to create <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> objects for them.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>



<a href="https://msdn.microsoft.com/64bdc08c-1902-448a-9eda-b557ab4bb095">Visual Basic Example</a>
 

 

