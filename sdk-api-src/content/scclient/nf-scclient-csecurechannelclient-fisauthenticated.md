---
UID: NF:scclient.CSecureChannelClient.fIsAuthenticated
title: CSecureChannelClient::fIsAuthenticated (scclient.h)
description: The fIsAuthenticated method verifies that a secure authenticated channel has been successfully established. This method is not used by applications.
helpviewer_keywords: ["CSecureChannelClient class [windows Media Device Manager]","fIsAuthenticated method","CSecureChannelClient.fIsAuthenticated","CSecureChannelClient::fIsAuthenticated","CSecureChannelClientfIsAuthenticated","fIsAuthenticated","fIsAuthenticated method [windows Media Device Manager]","fIsAuthenticated method [windows Media Device Manager]","CSecureChannelClient class","scclient/CSecureChannelClient::fIsAuthenticated","wmdm.csecurechannelclient_fisauthenticated"]
old-location: wmdm\csecurechannelclient_fisauthenticated.htm
tech.root: WMDM
ms.assetid: 9b9a529a-c652-48e1-b70d-e95e2e34e2c5
ms.date: 12/05/2018
ms.keywords: CSecureChannelClient class [windows Media Device Manager],fIsAuthenticated method, CSecureChannelClient.fIsAuthenticated, CSecureChannelClient::fIsAuthenticated, CSecureChannelClientfIsAuthenticated, fIsAuthenticated, fIsAuthenticated method [windows Media Device Manager], fIsAuthenticated method [windows Media Device Manager],CSecureChannelClient class, scclient/CSecureChannelClient::fIsAuthenticated, wmdm.csecurechannelclient_fisauthenticated
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CSecureChannelClient::fIsAuthenticated
 - scclient/CSecureChannelClient::fIsAuthenticated
dev_langs:
 - c++
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
---

# CSecureChannelClient::fIsAuthenticated


## -description

The <b>fIsAuthenticated</b> method verifies that a secure authenticated channel has been successfully established. This method is not used by applications.



## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method is used to ensure that a secure authentication channel has been established between components before allowing other operations. This includes calls by devices and storages prior to accessing and transferring data streams.

Applications do not need to call this method, but service providers call the corresponding <a href="/previous-versions/bb231600(v=vs.85)">CSecureChannelServer::fIsAuthenticated</a> method and return WMDM_E_NOTCERTIFIED if it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/WMDM/authenticating-the-application">Authenticating the Application</a>



<a href="/windows/desktop/WMDM/csecurechannelclient-class">CSecureChannelClient Class</a>
