---
UID: NF:faxcom.IFaxServer.put_ServerMapiProfile
title: IFaxServer::put_ServerMapiProfile (faxcom.h)
author: windows-sdk-content
description: Sets or retrieves the ServerMapiProfile property for a FaxServer object. The ServerMapiProfile property is a null-terminated string that contains the MAPI user profile that the fax server uses for routing incoming fax transmissions.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_servermapiprofile_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9nqd.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxServer interface [Fax Service],ServerMapiProfile property, IFaxServer.ServerMapiProfile, IFaxServer.get_ServerMapiProfile, IFaxServer.put_ServerMapiProfile, IFaxServer::ServerMapiProfile, IFaxServer::get_ServerMapiProfile, IFaxServer::put_ServerMapiProfile, ServerMapiProfile property [Fax Service], ServerMapiProfile property [Fax Service],IFaxServer interface, _mfax_ifaxserver_get_servermapiprofile, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_servermapiprofile_cpp, fax._mfax_ifaxserver_get_servermapiprofile, faxcom/IFaxServer::ServerMapiProfile, faxcom/IFaxServer::get_ServerMapiProfile, faxcom/IFaxServer::put_ServerMapiProfile, put_ServerMapiProfile
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
 - IFaxServer.ServerMapiProfile
 - IFaxServer.get_ServerMapiProfile
 - IFaxServer.put_ServerMapiProfile
 - IFaxServer.get_ServerMapiProfile
 - IFaxServer.put_ServerMapiProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::put_ServerMapiProfile


## -description


Sets or retrieves the <b>ServerMapiProfile</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>ServerMapiProfile</b> property is a null-terminated string that contains the MAPI user profile that the fax server uses for routing incoming fax transmissions.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This function is not supported in Windows XP.</div>
<div> </div>
The <b>IFaxServer::get_ServerMapiProfile</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692367(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692375(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

