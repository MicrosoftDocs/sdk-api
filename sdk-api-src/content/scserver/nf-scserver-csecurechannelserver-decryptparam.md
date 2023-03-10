---
UID: NF:scserver.CSecureChannelServer.DecryptParam
title: CSecureChannelServer::DecryptParam (scserver.h)
description: DecryptParam uses the session key of the secure authenticated channel to decrypt the data contained in a parameter.
helpviewer_keywords: ["CSecureChannelServer class [windows Media Device Manager]","DecryptParam method","CSecureChannelServer.DecryptParam","CSecureChannelServer::DecryptParam","CSecureChannelServerDecryptParam","DecryptParam","DecryptParam method [windows Media Device Manager]","DecryptParam method [windows Media Device Manager]","CSecureChannelServer class","scserver/CSecureChannelServer::DecryptParam","wmdm.csecurechannelserver_decryptparam"]
old-location: wmdm\csecurechannelserver_decryptparam.htm
tech.root: WMDM
ms.assetid: 42ccaf4a-02a4-432f-a0eb-b7852f0e5406
ms.date: 12/05/2018
ms.keywords: CSecureChannelServer class [windows Media Device Manager],DecryptParam method, CSecureChannelServer.DecryptParam, CSecureChannelServer::DecryptParam, CSecureChannelServerDecryptParam, DecryptParam, DecryptParam method [windows Media Device Manager], DecryptParam method [windows Media Device Manager],CSecureChannelServer class, scserver/CSecureChannelServer::DecryptParam, wmdm.csecurechannelserver_decryptparam
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
 - CSecureChannelServer::DecryptParam
 - scserver/CSecureChannelServer::DecryptParam
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
 - CSecureChannelServer.DecryptParam
---

# CSecureChannelServer::DecryptParam


## -description

<b>DecryptParam</b> uses the session key of the secure authenticated channel to decrypt the data contained in a parameter.

## -parameters

### -param pbData [in, out]

Pointer to the first byte of a data buffer containing the encrypted parameter that is to be decrypted.

### -param dwDataLen [in]

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

Components should copy the data to a temporary buffer before calling <b>DecryptParam</b> and then decrypt the temporary buffer. This method only needs to be called for encrypted parameters. See <a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Using Secure Authenticated Channels</a> for a table of methods that must use the message authentication code algorithm and encrypted parameters.


#### Examples

The following code shows a service provider's implementation of the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write">IMDSPObject::Write</a> method, which requires a service provider to decrypt data sent to it.


```cpp

HRESULT CMyStorage::Write(BYTE *pData, DWORD *pdwSize,
                                 BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwWritten = 0;
    BYTE    *pTmpData  = NULL;          // Temporary buffer to hold the 
                                        // data during decryption.
    BYTE     pTempMac[WMDM_MAC_LENGTH]; // Temporary MAC that will be 
                                        // copied into the abMac
                                        // out parameter.

    if( m_hFile == INVALID_HANDLE_VALUE )
    {
        return E_FAIL;
    }

    // Allocate the temporary buffer and copy the encrypted data into it.
    pTmpData = new BYTE [*pdwSize];
    if(!pTmpData)
        return E_OUTOFMEMORY;
    memcpy(pTmpData, pData, *pdwSize);

    // Decrypt the data.
    CHRg(g_pAppSCServer->DecryptParam(pTmpData, *pdwSize));

    // Check the MAC passed to the method. The MAC is built from
    // the data and data size parameters.
    // CORg is a macro that goes to the Error label on failure.
    HMAC hMAC;
    CORg(g_pAppSCServer->MACInit(&hMAC));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), *pdwSize));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(*pdwSize)));
    CORg(g_pAppSCServer->MACFinal(hMAC, pTempMac));

    // If the MAC values don't match, return an error.
    if (memcmp(abMac, pTempMac, WMDM_MAC_LENGTH) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
        goto Error;
    }

    // The MAC values matched, so write the decrypted data to a local file.
    if( WriteFile(m_hFile,pTmpData,*pdwSize,&dwWritten,NULL) ) 
    {
        hr = S_OK;
    }
    else 
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    *pdwSize = dwWritten;

Error:

    if( pTmpData )
    {
        delete [] pTmpData;
    }

    return hr;
}

```

## -see-also

<a href="/previous-versions/bb231586(v=vs.85)">CSecureChannelClient::DecryptParam</a>



<a href="/previous-versions/bb231587(v=vs.85)">CSecureChannelClient::EncryptParam</a>



<a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer Class</a>



<a href="/previous-versions/ms868509(v=msdn.10)">CSecureChannelServer::EncryptParam</a>