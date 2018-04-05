---
UID: NF:strmif.IAMStreamConfig.GetStreamCaps
title: IAMStreamConfig::GetStreamCaps method
author: windows-driver-content
description: The GetStreamCaps method retrieves a set of format capabilities.
old-location: dshow\iamstreamconfig_getstreamcaps.htm
old-project: DirectShow
ms.assetid: 9dd84847-2cae-42f2-a858-7106cd2ac075
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetStreamCaps method [DirectShow], GetStreamCaps method [DirectShow], IAMStreamConfig interface, GetStreamCaps,IAMStreamConfig.GetStreamCaps, IAMStreamConfig, IAMStreamConfig interface [DirectShow], GetStreamCaps method, IAMStreamConfig::GetStreamCaps, IAMStreamConfigGetStreamCaps, dshow.iamstreamconfig_getstreamcaps, strmif/IAMStreamConfig::GetStreamCaps
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMStreamConfig.GetStreamCaps
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMStreamConfig::GetStreamCaps method


## -description



The <b>GetStreamCaps</b> method retrieves a set of format capabilities.




## -parameters




### -param iIndex [in]

Specifies the format capability to retrieve, indexed from zero. To determine the number of capabilities that the pin supports, call the <a href="https://msdn.microsoft.com/355b8c4c-6d07-4d31-8dc5-ddc5ec2bf1cd">IAMStreamConfig::GetNumberOfCapabilities</a> method.


### -param ppmt




### -param pSCC [out]

Pointer to a byte array allocated by the caller. For video, use the <a href="https://msdn.microsoft.com/c4e68065-79d0-4e2e-abe5-2e5b6a51bd40">VIDEO_STREAM_CONFIG_CAPS</a> structure (see Remarks). For audio, use the <a href="https://msdn.microsoft.com/8a923e8e-173e-4258-ba81-7d398bd9c5fe">AUDIO_STREAM_CONFIG_CAPS</a> structure. To determine the required size of the array, call the <b>GetNumberOfCapabilities</b> method. The size is returned in the <i>piSize</i> parameter.


#### - pmt [out]

Address of a pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure. The method allocates the structure and fills it with a media type.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Specified index is too high.

</td>
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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid index.

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



This method returns two pieces of information:

<ul>
<li>The <i>pmt</i> parameter receives a filled-in <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure, which describes one supported output format.</li>
<li>The <i>pSCC</i> parameter receives a structure that contains additional format information. For video, <i>pSCC</i> receives a <a href="https://msdn.microsoft.com/c4e68065-79d0-4e2e-abe5-2e5b6a51bd40">VIDEO_STREAM_CONFIG_CAPS</a> structure. For audio, it receives an <a href="https://msdn.microsoft.com/8a923e8e-173e-4258-ba81-7d398bd9c5fe">AUDIO_STREAM_CONFIG_CAPS</a> structure.</li>
</ul>
<div class="alert"><b>Note</b>  Use of the <a href="https://msdn.microsoft.com/c4e68065-79d0-4e2e-abe5-2e5b6a51bd40">VIDEO_STREAM_CONFIG_CAPS</a> structure to configure a video device is deprecated. Although the caller must allocate the buffer, it should ignore the contents after the method returns. The capture device will return its supported formats through the <i>pmt</i> parameter.</div>
<div> </div>
To configure the output pin so that it uses this format, call the <a href="https://msdn.microsoft.com/8d64e5b6-e8fa-4678-92d4-3cbf92e13ddf">IAMStreamConfig::SetFormat</a> method and pass in the value of <i>pmt</i>.

Before calling <a href="https://msdn.microsoft.com/8d64e5b6-e8fa-4678-92d4-3cbf92e13ddf">SetFormat</a>, you can modify the <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure in <i>pmt</i>, using the information in <i>pSCC</i>. For example, an audio pin might return a default media type of 44-kHz, 16-bit stereo in the <i>pmt</i> parameter. Based on the values returned in the <a href="https://msdn.microsoft.com/8a923e8e-173e-4258-ba81-7d398bd9c5fe">AUDIO_STREAM_CONFIG_CAPS</a> structure, you might change this format to 8-bit mono before calling <b>SetFormat</b>.

The method allocates the memory for the <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that is returned in the <i>pmt</i> parameter. The caller must release the memory, including the format block. You can use the <a href="https://msdn.microsoft.com/970f6b2b-2bf5-418d-b4ae-637561cd6765">DeleteMediaType</a> helper function in the base class library. The caller must allocate the memory for the <i>pSCC</i> parameter.

On some compression filters, this method fails if the filter's input pin is not connected.

<b>Filter Developers</b>: For more information on implementing this method, see <a href="https://msdn.microsoft.com/f7466cfe-b13e-4ee9-82f9-0528ed97bf99">Exposing Capture and Compression Formats</a>.


#### Examples

The following example retrieves the first supported format (index zero) on a video output pin and then sets this format on the pin.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
int iCount, iSize;
BYTE *pSCC = NULL;
AM_MEDIA_TYPE *pmt;

hr = pConfig-&gt;GetNumberOfCapabilities(&amp;iCount, &amp;iSize);

pSCC = new BYTE[iSize];
if (pSCC == NULL)
{
    // TODO: Out of memory error.
}

// Get the first format.
hr = pConfig-&gt;GetStreamCaps(0, &amp;pmt, pSCC));
if (hr == S_OK)
{
    // TODO: Examine the format. If it's not suitable for some
    // reason, call GetStreamCaps with the next index value (up
    // to iCount). Otherwise, set the format:
    hr = pConfig-&gt;SetFormat(pmt);
    if (FAILED(hr))
    {
        // TODO: Error handling.
    }
    DeleteMediaType(pmt);
}
delete [] pSCC;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c171763e-9108-49a0-a4b7-855c6db0a71d">IAMStreamConfig Interface</a>
 

 

