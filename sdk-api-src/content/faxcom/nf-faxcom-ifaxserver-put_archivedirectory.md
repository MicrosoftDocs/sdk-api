---
UID: NF:faxcom.IFaxServer.put_ArchiveDirectory
title: IFaxServer::put_ArchiveDirectory (faxcom.h)
description: The IFaxServer::get_ArchiveDirectory method retrieves the ArchiveDirectory property for a FaxServer object. The ArchiveDirectory property is a null-terminated string that contains the location in which the fax server stores archived outbound faxes. (Put)
helpviewer_keywords: ["ArchiveDirectory property [Fax Service]","ArchiveDirectory property [Fax Service]","IFaxServer interface","IFaxServer interface [Fax Service]","ArchiveDirectory property","IFaxServer.ArchiveDirectory","IFaxServer.get_ArchiveDirectory","IFaxServer.put_ArchiveDirectory","IFaxServer::ArchiveDirectory","IFaxServer::get_ArchiveDirectory","IFaxServer::put_ArchiveDirectory","_mfax_ifaxserver_get_archivedirectory","fax._mfax_ifaxserver_client_mfax_ifaxserver_get_archivedirectory_cpp","fax._mfax_ifaxserver_get_archivedirectory","faxcom/IFaxServer::ArchiveDirectory","faxcom/IFaxServer::get_ArchiveDirectory","faxcom/IFaxServer::put_ArchiveDirectory","put_ArchiveDirectory"]
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_archivedirectory_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4fi1.htm
ms.date: 12/05/2018
ms.keywords: ArchiveDirectory property [Fax Service], ArchiveDirectory property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],ArchiveDirectory property, IFaxServer.ArchiveDirectory, IFaxServer.get_ArchiveDirectory, IFaxServer.put_ArchiveDirectory, IFaxServer::ArchiveDirectory, IFaxServer::get_ArchiveDirectory, IFaxServer::put_ArchiveDirectory, _mfax_ifaxserver_get_archivedirectory, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_archivedirectory_cpp, fax._mfax_ifaxserver_get_archivedirectory, faxcom/IFaxServer::ArchiveDirectory, faxcom/IFaxServer::get_ArchiveDirectory, faxcom/IFaxServer::put_ArchiveDirectory, put_ArchiveDirectory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxServer::put_ArchiveDirectory
 - faxcom/IFaxServer::put_ArchiveDirectory
dev_langs:
 - c++
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
---

# IFaxServer::put_ArchiveDirectory


## -description

The <b>IFaxServer::get_ArchiveDirectory</b> method retrieves the <b>ArchiveDirectory</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>ArchiveDirectory</b> property is a null-terminated string that contains the location in which the fax server stores archived outbound faxes.

This property is read/write.

## -parameters

## -remarks

Set the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-archiveoutboundfaxes-vb">ArchiveOutboundFaxes</a> property to <b>TRUE</b> to archive faxes in the directory specified by the <b>ArchiveDirectory</b> property. The fax server must have access to the directory to successfully store outbound fax transmissions. 
		

The <b>get_ArchiveDirectory</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-archiveoutboundfaxes-vb">IFaxServer::get_ArchiveOutboundFaxes</a>
