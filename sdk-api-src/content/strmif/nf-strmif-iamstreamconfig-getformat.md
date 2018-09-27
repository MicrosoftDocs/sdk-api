---
UID: NF:strmif.IAMStreamConfig.GetFormat
title: IAMStreamConfig::GetFormat
author: windows-sdk-content
description: The GetFormat method retrieves the current or preferred output format.
old-location: dshow\iamstreamconfig_getformat.htm
tech.root: DirectShow
ms.assetid: 5443141b-eb2c-412c-8bd1-7175e724b602
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetFormat, GetFormat method [DirectShow], GetFormat method [DirectShow],IAMStreamConfig interface, IAMStreamConfig interface [DirectShow],GetFormat method, IAMStreamConfig.GetFormat, IAMStreamConfig::GetFormat, IAMStreamConfigGetFormat, dshow.iamstreamconfig_getformat, strmif/IAMStreamConfig::GetFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMStreamConfig.GetFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMStreamConfig::GetFormat


## -description



The <code>GetFormat</code> method retrieves the current or preferred output format.




## -parameters




### -param ppmt

TBD




#### - pmt [out]

Address of a pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The input pin is not connected.

</td>
</tr>
</table>
 




## -remarks



If the pin is connected, this method returns the format that the pin is currently using. Otherwise, the method returns the pin's preferred format for the next pin connection. If you have already called the <a href="https://msdn.microsoft.com/8d64e5b6-e8fa-4678-92d4-3cbf92e13ddf">IAMStreamConfig::SetFormat</a> method to set the format, <code>GetFormat</code> returns the same format. If not, it returns the first format in the pin's list of preferred formats, as determined by the <a href="https://msdn.microsoft.com/288be4db-5236-40e5-bd92-d95b1bfb86fa">IPin::EnumMediaTypes</a> method.

The method allocates the memory for the <b>AM_MEDIA_TYPE</b> structure, fills in the structure, and returns it in the <i>pmt</i> parameter. The caller must release the memory, including the format block. You can use the <a href="https://msdn.microsoft.com/970f6b2b-2bf5-418d-b4ae-637561cd6765">DeleteMediaType</a> helper function in the base class library.

On some compression filters, the method fails if the filter's input pin is not connected.


#### Examples


```cpp

IAMStreamConfig *pConfig = NULL;
// Query the output pin for IAMStreamConfig (not shown).
AM_MEDIA_TYPE *pmt = NULL;
hr = pConfig->GetFormat(&pmt);
if (SUCCEEDED(hr))
{
    /* Examine the media type for any information you need. */
    DeleteMediaType(pmt);
}
pConfig->Release();

```





## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c171763e-9108-49a0-a4b7-855c6db0a71d">IAMStreamConfig Interface</a>
 

 

