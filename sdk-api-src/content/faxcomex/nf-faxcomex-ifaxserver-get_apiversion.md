---
UID: NF:faxcomex.IFaxServer.get_APIVersion
title: IFaxServer::get_APIVersion
author: windows-sdk-content
description: The APIVersion property is a value that indicates the version of the fax server API.
old-location: fax\_mfax_faxserver_apiversion_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_43vy.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: APIVersion property [Fax Service], APIVersion property [Fax Service],FaxServer object, FaxServer object [Fax Service],APIVersion property, FaxServer.APIVersion, IFaxServer.get_APIVersion, IFaxServer::get_APIVersion, _mfax_faxserver.apiversion, fax._mfax_faxserver_apiversion, fax._mfax_faxserver_apiversion_vb, get_APIVersion
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
 - FaxServer.APIVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxServer::get_APIVersion


## -description


The <b>APIVersion</b> property is a value that indicates the version of the fax server API.



This property is read-only.


## -parameters


## -remarks



In general, each new version of the fax server API is fully compatible with previous API versions. When connecting to a fax server using the Component Object Model (COM) objects, the API version of the fax server is not required because the COM layer performs the conversions and mapping to transparently support the fax API version of the server. However, if you want to detect the version of the fax server you are connected to, you can use the <b>APIVersion</b> property.




## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>



<a href="https://msdn.microsoft.com/80437d99-5b9f-4faa-8f09-ed91fc622d4b">Visual Basic Example</a>
 

 

