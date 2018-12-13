---
UID: NF:faxcom.IFaxServer.get_ServerMapiProfile
title: IFaxServer::get_ServerMapiProfile
author: windows-sdk-content
description: Sets or retrieves the ServerMapiProfile property for a FaxServer object. The ServerMapiProfile property is a null-terminated string that contains the MAPI user profile that the fax server uses for routing incoming fax transmissions.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_servermapiprofile_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9nqd.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxServer interface [Fax Service],ServerMapiProfile property, IFaxServer.ServerMapiProfile, IFaxServer.get_ServerMapiProfile, IFaxServer.put_ServerMapiProfile, IFaxServer::ServerMapiProfile, IFaxServer::get_ServerMapiProfile, IFaxServer::put_ServerMapiProfile, ServerMapiProfile property [Fax Service], ServerMapiProfile property [Fax Service],IFaxServer interface, _mfax_ifaxserver_get_servermapiprofile, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_servermapiprofile_cpp, fax._mfax_ifaxserver_get_servermapiprofile, faxcom/IFaxServer::ServerMapiProfile, faxcom/IFaxServer::get_ServerMapiProfile, faxcom/IFaxServer::put_ServerMapiProfile, get_ServerMapiProfile
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

# IFaxServer::get_ServerMapiProfile


## -description


Sets or retrieves the <b>ServerMapiProfile</b> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>ServerMapiProfile</b> property is a null-terminated string that contains the MAPI user profile that the fax server uses for routing incoming fax transmissions.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This function is not supported in Windows XP.</div>
<div> </div>
The <b>IFaxServer::get_ServerMapiProfile</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a>



<a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

