---
UID: NF:faxcomex.IFaxServer.GetDeviceProviders
title: IFaxServer::GetDeviceProviders
author: windows-driver-content
description: The IFaxServer::GetDeviceProviders method creates a IFaxDeviceProviders interface, a collection of fax service providers (FSPs) that are currently registered with the fax service.
old-location: fax\_mfax_faxserver_getdeviceproviders_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6xv7_cpp.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: GetDeviceProviders, GetDeviceProviders method [Fax Service], GetDeviceProviders method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],GetDeviceProviders method, IFaxServer.GetDeviceProviders, IFaxServer::GetDeviceProviders, _mfax_faxserver.getdeviceproviders_cpp, fax._mfax_faxserver_getdeviceproviders_cpp, faxcomex/IFaxServer::GetDeviceProviders
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxServer.GetDeviceProviders
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxServer::GetDeviceProviders


## -description


The <b>IFaxServer::GetDeviceProviders</b> method creates a <a href="https://msdn.microsoft.com/6c1bd4dd-a2bb-4ae7-a719-ec4506065c41">IFaxDeviceProviders</a> interface, a collection of fax service providers (FSPs) that are currently registered with the fax service. You can use the <b>IFaxDeviceProviders</b> interface to enumerate the FSPs associated with a fax server and to create and access <a href="https://msdn.microsoft.com/91899618-9164-4db4-94d3-a971db9f1ca0">IFaxDeviceProvider</a> interfaces for them.


## -parameters




### -param ppFaxDeviceProviders [out, retval]

Type: <b><a href="https://msdn.microsoft.com/6c1bd4dd-a2bb-4ae7-a719-ec4506065c41">IFaxDeviceProviders</a>**</b>

An address of a pointer that receives a <a href="https://msdn.microsoft.com/6c1bd4dd-a2bb-4ae7-a719-ec4506065c41">IFaxDeviceProviders</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>



<a href="https://msdn.microsoft.com/422003a1-7db2-4eff-97bd-8ca889a3e5f6">Visual Basic Example</a>
 

 

