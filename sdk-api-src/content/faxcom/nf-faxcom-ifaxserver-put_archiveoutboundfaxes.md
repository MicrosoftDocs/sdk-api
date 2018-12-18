---
UID: NF:faxcom.IFaxServer.put_ArchiveOutboundFaxes
title: IFaxServer::put_ArchiveOutboundFaxes
author: windows-sdk-content
description: Sets or retrieves the ArchiveOutboundFaxes property for a FaxServer object. The ArchiveOutboundFaxes property is a Boolean value that indicates whether the fax server archives outgoing fax transmissions.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_archiveoutboundfaxes_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7u43.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ArchiveOutboundFaxes property [Fax Service], ArchiveOutboundFaxes property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],ArchiveOutboundFaxes property, IFaxServer.ArchiveOutboundFaxes, IFaxServer.get_ArchiveOutboundFaxes, IFaxServer.put_ArchiveOutboundFaxes, IFaxServer::ArchiveOutboundFaxes, IFaxServer::get_ArchiveOutboundFaxes, IFaxServer::put_ArchiveOutboundFaxes, _mfax_ifaxserver_get_archiveoutboundfaxes, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_archiveoutboundfaxes_cpp, fax._mfax_ifaxserver_get_archiveoutboundfaxes, faxcom/IFaxServer::ArchiveOutboundFaxes, faxcom/IFaxServer::get_ArchiveOutboundFaxes, faxcom/IFaxServer::put_ArchiveOutboundFaxes, put_ArchiveOutboundFaxes
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

# IFaxServer::put_ArchiveOutboundFaxes


## -description


Sets or retrieves the <b>ArchiveOutboundFaxes</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>ArchiveOutboundFaxes</b> property is a Boolean value that indicates whether the fax server archives outgoing fax transmissions. 

This property is read/write.


## -parameters


## -remarks



The fax server ignores this property unless the <a href="https://msdn.microsoft.com/en-us/library/ms691828(v=VS.85).aspx">ArchiveDirectory</a> property is specified.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692367(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692375(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691828(v=VS.85).aspx">IFaxServer::get_ArchiveDirectory</a>
 

 

