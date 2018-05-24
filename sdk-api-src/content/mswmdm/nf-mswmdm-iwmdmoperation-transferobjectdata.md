---
UID: NF:mswmdm.IWMDMOperation.TransferObjectData
title: IWMDMOperation::TransferObjectData
author: windows-driver-content
description: The TransferObjectData method is called to allow the application to transfer a block of data to or from the computer.
old-location: wmdm\iwmdmoperation_transferobjectdata.htm
old-project: WMDM
ms.assetid: ba3f29d9-88cd-4050-aa9f-f9317745a16b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IWMDMOperation interface [windows Media Device Manager],TransferObjectData method, IWMDMOperation.TransferObjectData, IWMDMOperation::TransferObjectData, IWMDMOperationTransferObjectData, TransferObjectData, TransferObjectData method [windows Media Device Manager], TransferObjectData method [windows Media Device Manager],IWMDMOperation interface, mswmdm/IWMDMOperation::TransferObjectData, wmdm.iwmdmoperation_transferobjectdata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMOperation.TransferObjectData
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMOperation::TransferObjectData


## -description



The <b>TransferObjectData</b> method is called to allow the application to transfer a block of data to or from the computer.




## -parameters




### -param pData

Pointer to a buffer containing the data. This buffer is always allocated and freed by Windows Media Device Manager. Your application should never allocate or free this buffer.

<b>BeginRead</b>[in] During a read from device, incoming data that must be decrypted using the <a href="https://msdn.microsoft.com/4e19b86c-9efc-4c20-bac9-8cd6b944f69e">CSecureChannelClient::DecryptParam</a> method. The application does not need to deallocate the buffer.

<b>BeginWrite</b>[in, out] During a write to device, on input is a memory buffer <i>pdwSize</i> bytes long, allocated by Windows Media Device Manager. The application should fill this buffer with data that has been encrypted using the <a href="https://msdn.microsoft.com/7c71c2d4-b337-487f-a04a-87536f84f03e">CSecureChannelClient::EncryptParam</a> method.


### -param pdwSize

Pointer to a <b>DWORD</b> that specifies the transfer buffer size.

<b>BeginRead</b>[in, out] On input, the size of the incoming data in <i>pData</i>. On output, the amount of data the application has actually actually read.

<b>BeginWriteOn</b> input, the size of the <i>pData</i> buffer. On output, the actual size of the data sent out.


### -param abMac

Array of bytes specifying the message authentication code for the parameter data of this method.

<b>BeginRead</b>[in] A MAC generated from <i>pData</i> and <i>pdwSize</i> that the application should check after <i>pData</i> is decrypted, to verify that the data has not been modified.

<b>BeginWrite</b>[out] A MAC generated from <i>pData</i> and <i>pdwSize</i> before <i>pData</i> is encrypted.


## -returns



The application should return one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The read operation should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The read operation should be cancelled without finishing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred, and the read operation should be cancelled without finishing.

</td>
</tr>
</table>
 




## -remarks



The application can determine whether data is being read from or written to the device by monitoring whether <a href="https://msdn.microsoft.com/e72caaac-8992-4f11-8020-0455b3d730ad">BeginRead</a> or <a href="https://msdn.microsoft.com/1b35b026-1fc1-44e8-befc-211d3387bc92">BeginWrite</a> was called just before this method was called.


#### Examples

The following C++ code demonstrates how an application might implement <b>TransferObjectData</b> to handle file transfer itself. The code shown handles both reading data from and writing data to the device. The direction of data flow is indicated by a member variable <b>m_OperationStatus</b>, set in a prior call to <b>BeginRead</b> or <b>BeginWrite</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE* pMac)
{
    HRESULT hr = S_OK;

    // Verify parameters.
    if (pData == NULL || pdwSize == NULL || pMac == NULL || m_File == INVALID_HANDLE_VALUE) 
    {
        // TODO: Display the message: "Invalid argument in SetObjectTotalSize."
        return E_INVALIDARG;
    }
    if ((m_OperationStatus != OPERATION_READ) &amp;&amp; (m_OperationStatus != OPERATION_WRITE))
    {
        // TODO: Display the message: "Unable to determine direction of data transfer."
        return E_FAIL;
    }

    //////////////////////////////////////////////////////////////////////////
// Sending data to the device.
//////////////////////////////////////////////////////////////////////////
    if (m_OperationStatus == OPERATION_WRITE)
    {
        DWORD   dwReadLen;
        // The SAC is used to encrypt the data sent to the device.
        if (m_pSAC == NULL) 
        {
               // TODO: Display the message: "SAC not initialized in TransferObjectData."
            return E_FAIL;
        }

        // Read pdwSize bytes from the file into pData.
        dwReadLen = *pdwSize;
        if (ReadFile(m_File, pData, dwReadLen, pdwSize, NULL) == FALSE) 
        {
               // TODO: Display the message: "Couldn't read the file in TransferObjectData."
            return E_FAIL;
        }

        // If there is no more data, terminate the transfer.
        if (*pdwSize == 0)
        {
            return S_FALSE;
        }

        // Create the MAC to return to Windows Media Device Manager.
        HMAC hMAC;
        hr = m_pSAC-&gt;MACInit(&amp;hMAC);
        hr = m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(pData), *pdwSize);
        hr = m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD));
        hr = m_pSAC-&gt;MACFinal(hMAC, (BYTE*)pMac);
        if (hr != S_OK) return E_FAIL;

        // Encrypt the data to send to the service provider/device.
        hr = m_pSAC-&gt;EncryptParam((BYTE*)(pData), *pdwSize);
        if (hr != S_OK) 
        {
            return E_FAIL;
        }
    }
    //////////////////////////////////////////////////////////////////////////
// Receiving data from the device.
//////////////////////////////////////////////////////////////////////////
    else 
    {
        // Copy the data to a temporary file for decryption.
        BYTE *pTmpData = new BYTE [*pdwSize];
        if (pTmpData == NULL)
        {
            return E_OUTOFMEMORY;
        }
        memcpy(pTmpData, pData, *pdwSize);

        // Decrypt the pData Parameter
        hr = m_pSAC-&gt;DecryptParam(pTmpData, *pdwSize);
        
        // Verify the MAC of the decrypted data.
        HMAC hMAC;
        BYTE pTestMac[WMDM_MAC_LENGTH];
        hr = m_pSAC-&gt;MACInit(&amp;hMAC);
        hr = m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(pTmpData), *pdwSize);
        hr = m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(*pdwSize));
        hr = m_pSAC-&gt;MACFinal(hMAC, pTestMac);
        if ((memcmp(pMac, pTestMac, WMDM_MAC_LENGTH) != 0) || (hr != S_OK))
        {
            delete [] pTmpData;
            return WMDM_E_MAC_CHECK_FAILED;
        }

        // Write the data to file, and record the amount of data written.
        DWORD dwWritten = 0;
        if (WriteFile(m_File,pTmpData,*pdwSize,&amp;dwWritten,NULL))
        {
            hr = S_OK;
            *pdwSize = dwWritten;
        }
        else 
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
        if (pTmpData)
        {
            delete [] pTmpData;
        }
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6aef4138-0391-4edd-b4fc-d6d0ec3c735b">Encryption and Decryption</a>



<a href="https://msdn.microsoft.com/ff94191b-a0f2-4118-996c-d040f214fb9b">Handling File Transfers Manually</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7">Using Secure Authenticated Channels</a>
 

 

