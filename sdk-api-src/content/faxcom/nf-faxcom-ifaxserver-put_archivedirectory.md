---
UID: NF:faxcom.IFaxServer.put_ArchiveDirectory
title: IFaxServer::put_ArchiveDirectory (faxcom.h)
author: windows-sdk-content
description: The IFaxServer::get_ArchiveDirectory method retrieves the ArchiveDirectory property for a FaxServer object. The ArchiveDirectory property is a null-terminated string that contains the location in which the fax server stores archived outbound faxes.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_archivedirectory_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4fi1.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ArchiveDirectory property [Fax Service], ArchiveDirectory property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],ArchiveDirectory property, IFaxServer.ArchiveDirectory, IFaxServer.get_ArchiveDirectory, IFaxServer.put_ArchiveDirectory, IFaxServer::ArchiveDirectory, IFaxServer::get_ArchiveDirectory, IFaxServer::put_ArchiveDirectory, _mfax_ifaxserver_get_archivedirectory, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_archivedirectory_cpp, fax._mfax_ifaxserver_get_archivedirectory, faxcom/IFaxServer::ArchiveDirectory, faxcom/IFaxServer::get_ArchiveDirectory, faxcom/IFaxServer::put_ArchiveDirectory, put_ArchiveDirectory
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
---

# IFaxServer::put_ArchiveDirectory


## -description


The <b>IFaxServer::get_ArchiveDirectory</b> method retrieves the <b>ArchiveDirectory</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>ArchiveDirectory</b> property is a null-terminated string that contains the location in which the fax server stores archived outbound faxes.

This property is read/write.


## -parameters


## -remarks



Set the <a href="https://msdn.microsoft.com/en-us/library/ms692347(v=VS.85).aspx">ArchiveOutboundFaxes</a> property to <b>TRUE</b> to archive faxes in the directory specified by the <b>ArchiveDirectory</b> property. The fax server must have access to the directory to successfully store outbound fax transmissions. 
		

The <b>get_ArchiveDirectory</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.
		




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692367(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692375(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692347(v=VS.85).aspx">IFaxServer::get_ArchiveOutboundFaxes</a>
 

 

