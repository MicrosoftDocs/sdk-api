---
UID: NF:faxcom.IFaxServer.get_ArchiveOutboundFaxes
title: IFaxServer::get_ArchiveOutboundFaxes
author: windows-sdk-content
description: Sets or retrieves the ArchiveOutboundFaxes property for a FaxServer object. The ArchiveOutboundFaxes property is a Boolean value that indicates whether the fax server archives outgoing fax transmissions.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_archiveoutboundfaxes_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7u43.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ArchiveOutboundFaxes property [Fax Service], ArchiveOutboundFaxes property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],ArchiveOutboundFaxes property, IFaxServer.ArchiveOutboundFaxes, IFaxServer.get_ArchiveOutboundFaxes, IFaxServer.put_ArchiveOutboundFaxes, IFaxServer::ArchiveOutboundFaxes, IFaxServer::get_ArchiveOutboundFaxes, IFaxServer::put_ArchiveOutboundFaxes, _mfax_ifaxserver_get_archiveoutboundfaxes, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_archiveoutboundfaxes_cpp, fax._mfax_ifaxserver_get_archiveoutboundfaxes, faxcom/IFaxServer::ArchiveOutboundFaxes, faxcom/IFaxServer::get_ArchiveOutboundFaxes, faxcom/IFaxServer::put_ArchiveOutboundFaxes, get_ArchiveOutboundFaxes
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFaxServer.ArchiveOutboundFaxes
 - IFaxServer.get_ArchiveOutboundFaxes
 - IFaxServer.put_ArchiveOutboundFaxes
 - IFaxServer.get_ArchiveOutboundFaxes
 - IFaxServer.put_ArchiveOutboundFaxes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::get_ArchiveOutboundFaxes


## -description


Sets or retrieves the <b>ArchiveOutboundFaxes</b> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>ArchiveOutboundFaxes</b> property is a Boolean value that indicates whether the fax server archives outgoing fax transmissions. 

This property is read/write.


## -parameters


## -remarks



The fax server ignores this property unless the <a href="https://msdn.microsoft.com/1c266ddb-62dc-4faf-9761-1c8c08c0b125">ArchiveDirectory</a> property is specified.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a>



<a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a>



<a href="https://msdn.microsoft.com/1c266ddb-62dc-4faf-9761-1c8c08c0b125">IFaxServer::get_ArchiveDirectory</a>
 

 

