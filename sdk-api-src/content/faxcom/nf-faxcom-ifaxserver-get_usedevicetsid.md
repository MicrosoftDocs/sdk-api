---
UID: NF:faxcom.IFaxServer.get_UseDeviceTsid
title: IFaxServer::get_UseDeviceTsid
author: windows-sdk-content
description: Sets or retrieves the UseDeviceTsid property for a FaxServer object. The UseDeviceTsid property is a Boolean value that indicates whether the fax server uses the device's transmitting station identifier (TSID) instead of a user-specified TSID.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_usedevicetsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0xb8.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxServer interface [Fax Service],UseDeviceTsid property, IFaxServer.UseDeviceTsid, IFaxServer.get_UseDeviceTsid, IFaxServer.put_UseDeviceTsid, IFaxServer::UseDeviceTsid, IFaxServer::get_UseDeviceTsid, IFaxServer::put_UseDeviceTsid, UseDeviceTsid property [Fax Service], UseDeviceTsid property [Fax Service],IFaxServer interface, _mfax_ifaxserver_get_usedevicetsid, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_usedevicetsid_cpp, fax._mfax_ifaxserver_get_usedevicetsid, faxcom/IFaxServer::UseDeviceTsid, faxcom/IFaxServer::get_UseDeviceTsid, faxcom/IFaxServer::put_UseDeviceTsid, get_UseDeviceTsid
ms.topic: method
req.header: faxcom.h
req.include-header: 
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
req.lib: 
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxServer.UseDeviceTsid
 - IFaxServer.get_UseDeviceTsid
 - IFaxServer.put_UseDeviceTsid
 - IFaxServer.get_UseDeviceTsid
 - IFaxServer.put_UseDeviceTsid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::get_UseDeviceTsid


## -description


Sets or retrieves the <b>UseDeviceTsid</b> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>UseDeviceTsid</b> property is a Boolean value that indicates whether the fax server uses the device's transmitting station identifier (TSID) instead of a user-specified TSID.

This property is read/write.


## -parameters


## -remarks



To ensure that the TSID for a port is associated with outbound faxes, set the <b>UseDeviceTsid</b> property equal to <b>TRUE</b>. This overrides the TSID a user can optionally specify for an outbound fax by setting the <a href="https://msdn.microsoft.com/26d33ea3-a30d-4a04-9760-f637196db23d">Tsid</a> property. 
		




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a>



<a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a>



<a href="https://msdn.microsoft.com/26d33ea3-a30d-4a04-9760-f637196db23d">Tsid</a>
 

 

