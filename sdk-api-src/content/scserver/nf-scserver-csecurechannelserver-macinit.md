---
UID: NF:scserver.CSecureChannelServer.MACInit
title: CSecureChannelServer::MACInit (scserver.h)
description: The MACInit method acquires a message authentication code (MAC) channel for use in calls to the MACUpdate and MACFinal methods.
helpviewer_keywords: ["CSecureChannelServer class [windows Media Device Manager]","MACInit method","CSecureChannelServer.MACInit","CSecureChannelServer::MACInit","CSecureChannelServerMACInit","MACInit","MACInit method [windows Media Device Manager]","MACInit method [windows Media Device Manager]","CSecureChannelServer class","scserver/CSecureChannelServer::MACInit","wmdm.csecurechannelserver_macinit"]
old-location: wmdm\csecurechannelserver_macinit.htm
tech.root: WMDM
ms.assetid: 92161bf3-8e2f-4b4a-a09a-98e33637df27
ms.date: 12/05/2018
ms.keywords: CSecureChannelServer class [windows Media Device Manager],MACInit method, CSecureChannelServer.MACInit, CSecureChannelServer::MACInit, CSecureChannelServerMACInit, MACInit, MACInit method [windows Media Device Manager], MACInit method [windows Media Device Manager],CSecureChannelServer class, scserver/CSecureChannelServer::MACInit, wmdm.csecurechannelserver_macinit
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
 - CSecureChannelServer::MACInit
 - scserver/CSecureChannelServer::MACInit
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
 - CSecureChannelServer.MACInit
---

# CSecureChannelServer::MACInit


## -description

The <b>MACInit</b> method acquires a message authentication code (MAC) channel for use in calls to the <b>MACUpdate</b> and <b>MACFinal</b> methods.

## -parameters

### -param phMAC [out]

Pointer to a MAC handle.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>The phMAC parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>

## -remarks

The <b>MACInit</b> method begins a message authentication code (MAC) session. This method must be called every time a (MAC) is required. <b>MACUpdate</b> and <b>MACFinal</b> must be called sequentially after <b>MACInit</b>. After <b>MACFinal</b>, <b>MACInit</b> must be called again to acquire a new handle.


#### Examples


```cpp

g_pAppSCServer = new CsecureChannelServer();
if( dwRead )
{
    // MAC the parameters.
    HMAC hMAC;
    
    g_pAppSCServer->MACInit(&hMAC);
    g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), dwRead);
    g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD));
    g_pAppSCServer->MACFinal(hMAC, abMac);
    
    g_pAppSCServer->EncryptParam(pTmpData, dwRead);
    
    memcpy(pData, pTmpData, dwRead);
    }

```

## -see-also

<a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer Class</a>



<a href="/previous-versions/ms868513(v=msdn.10)">CSecureChannelServer::MACFinal</a>



<a href="/previous-versions/ms868515(v=msdn.10)">CSecureChannelServer::MACUpdate</a>



<a href="/windows/desktop/WMDM/message-authentication">Message Authentication</a>