---
UID: NF:scclient.CSecureChannelClient.fIsAuthenticated
title: CSecureChannelClient::fIsAuthenticated
author: windows-sdk-content
description: The fIsAuthenticated method verifies that a secure authenticated channel has been successfully established. This method is not used by applications.
old-location: wmdm\csecurechannelclient_fisauthenticated.htm
tech.root: WMDM
ms.assetid: 9b9a529a-c652-48e1-b70d-e95e2e34e2c5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CSecureChannelClient interface [windows Media Device Manager],fIsAuthenticated method, CSecureChannelClient.fIsAuthenticated, CSecureChannelClient::fIsAuthenticated, CSecureChannelClientfIsAuthenticated, fIsAuthenticated, fIsAuthenticated method [windows Media Device Manager], fIsAuthenticated method [windows Media Device Manager],CSecureChannelClient interface, scclient/CSecureChannelClient::fIsAuthenticated, wmdm.csecurechannelclient_fisauthenticated
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: scclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - CSecureChannelClient.fIsAuthenticated
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CSecureChannelClient::fIsAuthenticated


## -description



The <b>fIsAuthenticated</b> method verifies that a secure authenticated channel has been successfully established. This method is not used by applications.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method is used to ensure that a secure authentication channel has been established between components before allowing other operations. This includes calls by devices and storages prior to accessing and transferring data streams.

Applications do not need to call this method, but service providers call the corresponding <a href="https://msdn.microsoft.com/673d3bf6-27ba-4d91-b485-1171bc47a0d0">CSecureChannelServer::fIsAuthenticated</a> method and return WMDM_E_NOTCERTIFIED if it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/011815fa-d55c-4abc-9ec8-55d754827342">Authenticating the Application</a>



<a href="https://msdn.microsoft.com/f02220b8-0d1c-416c-97ea-e5e7455fcbba">CSecureChannelClient Class</a>
 

 

