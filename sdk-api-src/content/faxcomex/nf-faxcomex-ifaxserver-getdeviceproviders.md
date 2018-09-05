---
UID: NF:faxcomex.IFaxServer.GetDeviceProviders
title: IFaxServer::GetDeviceProviders
author: windows-sdk-content
description: The GetDeviceProviders method creates a FaxDeviceProviders object, a collection of fax service providers (FSPs) that are currently registered with the fax service.
old-location: fax\_mfax_faxserver_getdeviceproviders.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6xv7.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxServer object [Fax Service],GetDeviceProviders method, FaxServer.GetDeviceProviders, GetDeviceProviders, GetDeviceProviders method [Fax Service], GetDeviceProviders method [Fax Service],FaxServer object, IFaxServer.GetDeviceProviders, IFaxServer::GetDeviceProviders, _mfax_faxserver.getdeviceproviders, fax._mfax_faxserver_getdeviceproviders
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.redist: 
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
 - FaxServer.GetDeviceProviders
 - IFaxServer.GetDeviceProviders
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxServer::GetDeviceProviders


## -description


The <b>GetDeviceProviders</b> method creates a <a href="https://msdn.microsoft.com/3abb80d7-fedf-469d-b17a-604ca78f4b8b">FaxDeviceProviders</a> object, a collection of fax service providers (FSPs) that are currently registered with the fax service. You can use the <b>FaxDeviceProviders</b> object to enumerate the FSPs associated with a fax server and to create and access <a href="https://msdn.microsoft.com/ef32eb3d-e158-4740-82f5-661d5eded88c">FaxDeviceProvider</a> objects for them.


## -parameters




### -param ppFaxDeviceProviders






## -returns



Type: <b><a href="https://msdn.microsoft.com/3abb80d7-fedf-469d-b17a-604ca78f4b8b">FaxDeviceProviders</a>**</b>

A <a href="https://msdn.microsoft.com/3abb80d7-fedf-469d-b17a-604ca78f4b8b">FaxDeviceProviders</a> object.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>



<a href="https://msdn.microsoft.com/422003a1-7db2-4eff-97bd-8ca889a3e5f6">Visual Basic Example</a>
 

 

