---
UID: NF:scserver.CSecureChannelServer.fIsAuthenticated
title: CSecureChannelServer::fIsAuthenticated (scserver.h)
description: The fIsAuthenticated method verifies that a Secure Authenticated Channel has been successfully established.
helpviewer_keywords: ["CSecureChannelServer class [windows Media Device Manager]","fIsAuthenticated method","CSecureChannelServer.fIsAuthenticated","CSecureChannelServer::fIsAuthenticated","CSecureChannelServerfIsAuthenticated","fIsAuthenticated","fIsAuthenticated method [windows Media Device Manager]","fIsAuthenticated method [windows Media Device Manager]","CSecureChannelServer class","scserver/CSecureChannelServer::fIsAuthenticated","wmdm.csecurechannelserver_fisauthenticated"]
old-location: wmdm\csecurechannelserver_fisauthenticated.htm
tech.root: WMDM
ms.assetid: 673d3bf6-27ba-4d91-b485-1171bc47a0d0
ms.date: 12/05/2018
ms.keywords: CSecureChannelServer class [windows Media Device Manager],fIsAuthenticated method, CSecureChannelServer.fIsAuthenticated, CSecureChannelServer::fIsAuthenticated, CSecureChannelServerfIsAuthenticated, fIsAuthenticated, fIsAuthenticated method [windows Media Device Manager], fIsAuthenticated method [windows Media Device Manager],CSecureChannelServer class, scserver/CSecureChannelServer::fIsAuthenticated, wmdm.csecurechannelserver_fisauthenticated
req.header: scserver.h
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
 - CSecureChannelServer::fIsAuthenticated
 - scserver/CSecureChannelServer::fIsAuthenticated
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
 - CSecureChannelServer.fIsAuthenticated
---

# CSecureChannelServer::fIsAuthenticated


## -description

The <b>fIsAuthenticated</b> method verifies that a <a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Secure Authenticated Channel</a> has been successfully established.



## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method is used to ensure that a secure authenticated channel has been established between components before allowing certain operations. This includes calls by devices and storages prior to accessing and transferring data streams. You should confirm that this method returns <b>TRUE</b> before calling other top-level methods on the component.

Applications do not need to call the <b>fIsAuthenticated</b> method, but service providers do. They should call this method for all exposed APIs and return WMDM_E_NOTCERTIFIED if it returns <b>FALSE</b>.


#### Examples

The following code shows a service provider's implementation of <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getversion">IMDSPDevice::GetVersion</a>. This method verifies that a secure authenticated channel has been established before returning the version.


```cpp

HRESULT CMyDevice::GetVersion(DWORD * pdwVersion)
{
    HRESULT hr
 = S_OK;
    
    if(g_pAppSCServer == NULL)
        return E_FAIL;

    if (!(g_pAppSCServer->fIsAuthenticated()))
    {
        return WMDM_E_NOTCERTIFIED;
    }
    *pdwVersion = 1;
    return hr;
}

```

## -see-also

<a href="/previous-versions/ms868497(v=msdn.10)">CSecureChannelClient::fIsAuthenticated</a>



<a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer Class</a>
