---
UID: NF:faxcomex.IFaxServer.GetDeviceProviders
title: IFaxServer::GetDeviceProviders
author: windows-sdk-content
description: The GetDeviceProviders method creates a FaxDeviceProviders object, a collection of fax service providers (FSPs) that are currently registered with the fax service.
old-location: fax\_mfax_faxserver_getdeviceproviders.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6xv7.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FaxServer object [Fax Service],GetDeviceProviders method, FaxServer.GetDeviceProviders, GetDeviceProviders, GetDeviceProviders method [Fax Service], GetDeviceProviders method [Fax Service],FaxServer object, IFaxServer.GetDeviceProviders, IFaxServer::GetDeviceProviders, _mfax_faxserver.getdeviceproviders, fax._mfax_faxserver_getdeviceproviders
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


The <b>GetDeviceProviders</b> method creates a <a href="https://msdn.microsoft.com/library/ms687073(v=VS.85).aspx">FaxDeviceProviders</a> object, a collection of fax service providers (FSPs) that are currently registered with the fax service. You can use the <b>FaxDeviceProviders</b> object to enumerate the FSPs associated with a fax server and to create and access <a href="https://msdn.microsoft.com/library/ms684890(v=VS.85).aspx">FaxDeviceProvider</a> objects for them.


## -parameters




### -param ppFaxDeviceProviders






## -returns



Type: <b><a href="https://msdn.microsoft.com/library/ms687073(v=VS.85).aspx">FaxDeviceProviders</a>**</b>

A <a href="https://msdn.microsoft.com/library/ms687073(v=VS.85).aspx">FaxDeviceProviders</a> object.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/library/ms689109(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/library/ms689110(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/library/ms693462(v=VS.85).aspx">Visual Basic Example</a>
 

 

