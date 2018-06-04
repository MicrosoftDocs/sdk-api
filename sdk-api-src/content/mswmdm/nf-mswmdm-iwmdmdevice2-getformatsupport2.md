---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMDMDevice2::GetFormatSupport2


## -description



The <b>GetFormatSupport2</b> method retrieves the formats supported by the device, including audio and video codecs, and MIME file formats.




## -parameters




### -param dwFlags [in]

<b>DWORD</b> specifying audio formats, video formats, and MIME types. This flag specifies what the application is requesting the service provider to fill in. The caller can set one or more of the following three values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WMDM_GET_FORMAT_SUPPORT_AUDIO</td>
<td>Service provider should fill in audio parameters.</td>
</tr>
<tr>
<td>WMDM_GET_FORMAT_SUPPORT_VIDEO</td>
<td>Service provider should fill in video parameters.</td>
</tr>
<tr>
<td>WMDM_GET_FORMAT_SUPPORT_FILE</td>
<td>Service provider should fill in file parameters.</td>
</tr>
</table>
 


### -param ppAudioFormatEx [out]

Pointer to an array of <b>_WAVEFORMATEX</b> structures specifying information about audio codecs and bit rates supported by the device. The memory for this parameter is allocated by Windows Media Device Manager, and must be released by the caller with the Win32 function <b>CoTaskMemFree</b>.


### -param pnAudioFormatCount [out]

Pointer to an integer specifying the audio format count.


### -param ppVideoFormatEx [out]

Pointer to an array of <b>_VIDEOFORMATEX</b> structures specifying information about video codes and formats supported by the device. The memory for this parameter is allocated by Windows Media Device Manager, and must be released by the caller with the Win32 function <b>CoTaskMemFree</b>.


### -param pnVideoFormatCount [out]

Pointer to an integer specifying the video format count.


### -param ppFileType [out]

Pointer to an array of <b>WMFILECAPABILITIES</b> file-type objects. The memory for this parameter is allocated by Windows Media Device Manager, and must be released by the caller with the Win32 function <b>CoTaskMemFree</b>.


### -param pnFileTypeCount [out]

Pointer to an integer specifying the file-type count.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method extends <a href="https://msdn.microsoft.com/a917660d-300f-4ac4-befe-a3f78172411e">IWMDMDevice::GetFormatSupport</a> to handle video formats. The recommended method for getting format support, however, is <a href="https://msdn.microsoft.com/728df998-748b-4c53-b5a6-3a6ccae0d7e4">IWMDMDevice3::GetFormatCapability</a>. If <b>GetFormatCapability</b> isn't supported, the device will probably not support video, and <b>GetFormatSupport</b> is probably sufficient.




## -see-also




<a href="https://msdn.microsoft.com/dd139816-dc8c-4e73-9a21-67287bfe6405">Discovering Device Format Capabilities</a>



<a href="https://msdn.microsoft.com/d8dcbde1-24ae-4ca6-aaf4-2d1511102ae9">IWMDMDevice2 Interface</a>



<a href="https://msdn.microsoft.com/728df998-748b-4c53-b5a6-3a6ccae0d7e4">IWMDMDevice3::GetFormatCapability</a>
 

 

