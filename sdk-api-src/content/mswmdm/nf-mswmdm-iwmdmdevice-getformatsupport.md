---
UID: NF:mswmdm.IWMDMDevice.GetFormatSupport
title: IWMDMDevice::GetFormatSupport
author: windows-sdk-content
description: The GetFormatSupport method retrieves all the formats supported by the device, including codecs and file formats.
old-location: wmdm\iwmdmdevice_getformatsupport.htm
tech.root: WMDM
ms.assetid: a917660d-300f-4ac4-befe-a3f78172411e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetFormatSupport, GetFormatSupport method [windows Media Device Manager], GetFormatSupport method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetFormatSupport method, IWMDMDevice.GetFormatSupport, IWMDMDevice::GetFormatSupport, IWMDMDeviceGetFormatSupport, mswmdm/IWMDMDevice::GetFormatSupport, wmdm.iwmdmdevice_getformatsupport
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
 - IWMDMDevice.GetFormatSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mswmdm.h
: 
- IWMDMDevice.GetFormatSupport
: 
---

# IWMDMDevice::GetFormatSupport


## -description



The <b>GetFormatSupport</b> method retrieves all the formats supported by the device, including codecs and file formats.




## -parameters




### -param ppFormatEx [out]

Pointer to an array of <a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a> structures specifying information about codecs and bit rates supported by the device. Windows Media Device Manager allocates the memory for this parameter; the caller must free it using <b>CoTaskMemFree</b>.


### -param pnFormatCount [out]

Pointer to the number of elements in the <i>ppFormatEx</i> array.


### -param pppwszMimeType [out]

Pointer to an array describing file formats and digital rights management schemes supported by the device. Windows Media Device Manager allocates the memory for this parameter; the caller must free it using <b>CoTaskMemFree</b>.


### -param pnMimeTypeCount [out]

Pointer to the number of elements in the <i>pppwszMimeType</i> array.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The recommended way to retrieve device-supported formats is <a href="https://msdn.microsoft.com/728df998-748b-4c53-b5a6-3a6ccae0d7e4">IWMDMDevice3::GetFormatCapability</a>.


#### Examples

The following C++ function retrieves various device capabilities.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Function to print out device caps for a device that supports
// only IWMDMDevice.
void GetCaps(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get all capabilities for audio and mime support.
    _WAVEFORMATEX* pAudioFormats;
    LPWSTR* pMimeFormats;
    UINT numAudioFormats = 0;
    UINT numMimeFormats = 0;
    hr = pDevice-&gt;GetFormatSupport(
        &amp;pAudioFormats,
        &amp;numAudioFormats,
        &amp;pMimeFormats,
        &amp;numMimeFormats);

    HANDLE_HR(hr, "Got audio and mime formats in GetCaps IWMDMDevice", "Couldn't get audio and mime formats in GetCaps IWMDMDevice");

    // Print out audio format data.
    if (numAudioFormats &gt; 0)
    {
        / /TODO: Display a banner to precede the supported formats.
    }
    else
    {
        // TODO: Display a message indicating that no formats are supported.
    }
    for(int i = 0; i &lt; numAudioFormats; i++)
    {
        // TODO: Display a configuration value.
        PrintWaveFormatGuid(pAudioFormats[i].wFormatTag);
        // TODO: Display a max channel value.
        // TODO: Display a max samples/second value.
        // TODO: Display the max bytes/second value.
        // TODO: Display the block alignment value.
        // TODo: Display the max bits/sample value.
    }

    // Print out MIME formats.
    if (numMimeFormats &gt; 0)
        // TODO: Display a banner for the MIME format listing.
    else
        / /TODO: Display a message indicating that no MIME formats are supported.
    for(i = 0; i &lt; numMimeFormats; i++)
    {
        // TODO: Display each individual MIME format.
    }

e_Exit:
    return;

}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dd139816-dc8c-4e73-9a21-67287bfe6405">Discovering Device Format Capabilities</a>



<a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice Interface</a>



<a href="https://msdn.microsoft.com/728df998-748b-4c53-b5a6-3a6ccae0d7e4">IWMDMDevice3::GetFormatCapability</a>



<a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a>
 

 

