---
UID: NF:faxcom.IFaxServer.get_ArchiveDirectory
title: IFaxServer::get_ArchiveDirectory
author: windows-sdk-content
description: The IFaxServer::get_ArchiveDirectory method retrieves the ArchiveDirectory property for a FaxServer object. The ArchiveDirectory property is a null-terminated string that contains the location in which the fax server stores archived outbound faxes.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_archivedirectory_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4fi1.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ArchiveDirectory property [Fax Service], ArchiveDirectory property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],ArchiveDirectory property, IFaxServer.ArchiveDirectory, IFaxServer.get_ArchiveDirectory, IFaxServer.put_ArchiveDirectory, IFaxServer::ArchiveDirectory, IFaxServer::get_ArchiveDirectory, IFaxServer::put_ArchiveDirectory, _mfax_ifaxserver_get_archivedirectory, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_archivedirectory_cpp, fax._mfax_ifaxserver_get_archivedirectory, faxcom/IFaxServer::ArchiveDirectory, faxcom/IFaxServer::get_ArchiveDirectory, faxcom/IFaxServer::put_ArchiveDirectory, get_ArchiveDirectory
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
 - IFaxServer.ArchiveDirectory
 - IFaxServer.get_ArchiveDirectory
 - IFaxServer.put_ArchiveDirectory
 - IFaxServer.get_ArchiveDirectory
 - IFaxServer.put_ArchiveDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcom.h
: 
- IFaxServer.get_ArchiveDirectory
: 
---

# IFaxServer::get_ArchiveDirectory


## -description


The <b>IFaxServer::get_ArchiveDirectory</b> method retrieves the <b>ArchiveDirectory</b> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>ArchiveDirectory</b> property is a null-terminated string that contains the location in which the fax server stores archived outbound faxes.

This property is read/write.


## -parameters


## -remarks



Set the <a href="https://msdn.microsoft.com/8cf29336-f41d-4357-a6ea-c0b8ca3344ba">ArchiveOutboundFaxes</a> property to <b>TRUE</b> to archive faxes in the directory specified by the <b>ArchiveDirectory</b> property. The fax server must have access to the directory to successfully store outbound fax transmissions. 
		

The <b>get_ArchiveDirectory</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.
		




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a>



<a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>



<a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a>



<a href="https://msdn.microsoft.com/8cf29336-f41d-4357-a6ea-c0b8ca3344ba">IFaxServer::get_ArchiveOutboundFaxes</a>
 

 

