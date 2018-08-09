---
UID: NF:faxcomex.IFaxServer.GetDevices
title: IFaxServer::GetDevices
author: windows-sdk-content
description: The GetDevices method creates a FaxDevices object, a collection of all the fax devices exposed by all the fax service providers (FSPs) currently registered with the fax service.
old-location: fax\_mfax_faxserver_getdevices.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7hrn.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
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


The <b>GetDevices</b> method creates a <a href="https://msdn.microsoft.com/en-us/library/ms684819(v=VS.85).aspx">FaxDevices</a> object, a collection of all the fax devices exposed by all the fax service providers (FSPs) currently registered with the fax service.


## -parameters




### -param ppFaxDevices






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms684819(v=VS.85).aspx">FaxDevices</a>**</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms684819(v=VS.85).aspx">FaxDevices</a> object.




## -remarks



You can use the <a href="https://msdn.microsoft.com/en-us/library/ms684819(v=VS.85).aspx">FaxDevices</a> object to enumerate the fax devices associated with a connected fax server and to create <a href="https://msdn.microsoft.com/en-us/library/ms686192(v=VS.85).aspx">FaxDevice</a> objects for them.

To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms689109(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689110(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693400(v=VS.85).aspx">Visual Basic Example</a>
 

 

