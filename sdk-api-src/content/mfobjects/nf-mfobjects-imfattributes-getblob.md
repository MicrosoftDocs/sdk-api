---
UID: NF:mfobjects.IMFAttributes.GetBlob
title: IMFAttributes::GetBlob
author: windows-sdk-content
description: Retrieves a byte array associated with a key. This method copies the array into a caller-allocated buffer.
old-location: mf\imfattributes_getblob.htm
tech.root: medfound
ms.assetid: 68528db7-90df-4abe-a957-ffb8c3f12cef
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 68528db7-90df-4abe-a957-ffb8c3f12cef, GetBlob, GetBlob method [Media Foundation], GetBlob method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetBlob method, IMFAttributes.GetBlob, IMFAttributes::GetBlob, mf.imfattributes_getblob, mfobjects/IMFAttributes::GetBlob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes.GetBlob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAttributes::GetBlob


## -description



Retrieves a byte array associated with a key. This method copies the array into a caller-allocated buffer.




## -parameters




### -param guidKey [in]

GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_BLOB</b>.


### -param pBuf [out]

Pointer to a buffer allocated by the caller. If the key is found and the value is a byte array, the method copies the array into this buffer. To find the required size of the buffer, call <a href="https://msdn.microsoft.com/93ab65e7-2168-4cfb-a871-b39554ba66e0">IMFAttributes::GetBlobSize</a>.


### -param cbBufSize [in]

The size of the <i>pBuf</i> buffer, in bytes.


### -param pcbBlobSize [out]

Receives the size of the byte array. This parameter can be <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_NOT_SUFFICIENT_BUFFER</b></b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to the array.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_ATTRIBUTENOTFOUND</b></b></dt>
</dl>
</td>
<td width="60%">
The specified key was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALIDTYPE</b></b></dt>
</dl>
</td>
<td width="60%">
The attribute value is not a byte array.

</td>
</tr>
</table>
 




## -remarks



You can also use the <a href="https://msdn.microsoft.com/380e0e3a-b5c5-4d31-8793-417262377fef">IMFAttributes::GetAllocatedBlob</a> method, which allocates the buffer to hold the byte array.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples

The following code example shows how to get an attribute whose value is a byte array.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HRESULT AttributeGetBlob(IMFAttributes *pAttributes)
{
    HRESULT hr = S_OK;
    UINT32 cbBlob = 0;
    BYTE *pBlob = NULL;

    hr = pAttributes-&gt;GetBlobSize(MY_ATTRIBUTE, &amp;cbBlob);
    
    if (SUCCEEDED(hr))
    {
        pBlob = new BYTE[cbBlob];
        if (pBlob == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = pAttributes-&gt;GetBlob(MY_ATTRIBUTE, pBlob, cbBlob, &amp;cbBlob);
    }

    if (pBlob)
    {
        delete [] pBlob;
    }
    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/1844fbe2-0a07-4c0c-9ffe-4c59fc01f793">MF_ATTRIBUTE_TYPE</a>
 

 

