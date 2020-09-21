---
UID: NF:scserver.CSecureChannelServer.EncryptParam
title: CSecureChannelServer::EncryptParam (scserver.h)
description: The EncryptParam method uses the session key of the secure authenticated channel to encrypt the data contained in a parameter.
helpviewer_keywords: ["CSecureChannelServer class [windows Media Device Manager]","EncryptParam method","CSecureChannelServer.EncryptParam","CSecureChannelServer::EncryptParam","CSecureChannelServerEncryptParam","EncryptParam","EncryptParam method [windows Media Device Manager]","EncryptParam method [windows Media Device Manager]","CSecureChannelServer class","scserver/CSecureChannelServer::EncryptParam","wmdm.csecurechannelserver_encryptparam"]
old-location: wmdm\csecurechannelserver_encryptparam.htm
tech.root: WMDM
ms.assetid: dbfc72a6-acd5-40c2-8951-ab90e5c4d752
ms.date: 12/05/2018
ms.keywords: CSecureChannelServer class [windows Media Device Manager],EncryptParam method, CSecureChannelServer.EncryptParam, CSecureChannelServer::EncryptParam, CSecureChannelServerEncryptParam, EncryptParam, EncryptParam method [windows Media Device Manager], EncryptParam method [windows Media Device Manager],CSecureChannelServer class, scserver/CSecureChannelServer::EncryptParam, wmdm.csecurechannelserver_encryptparam
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
 - CSecureChannelServer::EncryptParam
 - scserver/CSecureChannelServer::EncryptParam
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
 - CSecureChannelServer.EncryptParam
---

# CSecureChannelServer::EncryptParam


## -description

The <b>EncryptParam</b> method uses the session key of the secure authenticated channel to encrypt the data contained in a parameter.

## -parameters

### -param pbData

Pointer to the first byte of a data buffer containing the parameter that is to be encrypted.

### -param dwDataLen

Pointer to a <b>DWORD</b> specifying the length of the buffer to which <i>pbData</i> points.

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
<td>A parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>

## -remarks

Certain parameters, listed in the tables under <a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Using Secure Authenticated Channels</a>, must be included in the message authentication code (MAC) and must be encrypted before the call for data transfer in both directions. Call <b>EncryptParam</b> to encrypt the specified parameters. Do not encrypt any parameters that do not require it.


#### Examples

The following code demonstrates a service provider's implementation of <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read">IMDSPObject::Read</a>. This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.


```cpp

HRESULT CMyStorage::Read(
    BYTE  *pData,
    DWORD *pdwSize,
    BYTE   abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwToRead;         // Bytes to read.
    DWORD    dwRead   = NULL;  // Bytes read.
    BYTE    *pTmpData = NULL;  // Temporary buffer to hold data before it 
                               // is copied out to pData.

    // Use a global CSecureChannelServer member to verify that the client 
    // is authenticated.
    if (!(g_pAppSCServer->fIsAuthenticated()))
    {
        return WMDM_E_NOTCERTIFIED;
    }
    

    // Verify that the handle to the file to read is valid.
    if(m_hFile == INVALID_HANDLE_VALUE)
    {
        return E_FAIL;
    }

    // Create a buffer to hold the data read.    
    dwToRead = *pdwSize;
    pTmpData = new BYTE [dwToRead] ;
    if(!pTmpData)
        return E_OUTOFMEMORY;

    // Read data into the temporary buffer.
    if(ReadFile(m_hFile,(LPVOID)pTmpData,dwToRead,&dwRead,NULL)) 
    { 
        *pdwSize = dwRead; 

        if( dwRead )
        {
            // Create a MAC from all the parameters.
            // CORg is a macro that goes to Error label on failure.
            // MAC consists of data and size of data.
            HMAC hMAC;
            
            CORg(g_pAppSCServer->MACInit(&hMAC));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), dwRead));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD)));
            CORg(g_pAppSCServer->MACFinal(hMAC, abMac));
            
            // Encrypt the data.
            CORg(g_pAppSCServer->EncryptParam(pTmpData, dwRead));
            
            // Copy the data from the temporary buffer into the out param.
            memcpy(pData, pTmpData, dwRead);
        }
    
        hr = S_OK; 
    }
    else
    { 
        *pdwSize = 0; 

        hr = E_FAIL; 
    }

Error:

    if(pTmpData) 
    {
        delete [] pTmpData;
    }

    return hr;
} 

```

## -see-also

<a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer Class</a>



<a href="/previous-versions/bb231598(v=vs.85)">CSecureChannelServer::DecryptParam</a>