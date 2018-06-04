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

# IMDSPDevice2::GetFormatSupport2


## -description



The <b>GetFormatSupport2</b> method gets the formats supported by a device, including audio and video codecs, and MIME file formats.




## -parameters




### -param dwFlags [in]

<b>DWORD</b> containing audio formats, video formats, and MIME types. This flag specifies what the application is requesting the service provider to fill in. The caller can set one or more of the following three values.

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

Pointer to an array of <a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a> structures containing information about audio codecs and bit rates supported by the device.


### -param pnAudioFormatCount [out]

Pointer to an integer containing the audio format count.


### -param ppVideoFormatEx [out]

Pointer to an array of <a href="https://msdn.microsoft.com/5a39d66e-8dbc-4572-8370-14f722b6c906">_VIDEOINFOHEADER</a> structures containing information about video codecs and formats supported by the device.


### -param pnVideoFormatCount [out]

Pointer to an integer containing the video format count.


### -param ppFileType [out]

Pointer to an array of <a href="https://msdn.microsoft.com/30307343-f55e-4695-9ae8-b938617d749d">WMFILECAPABILITIES</a> structures containing information about file types supported by the device.


### -param pnFileTypeCount [out]

Pointer to an integer containing the file format count.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/a53052a1-89f4-4571-9eee-031e0049a92e">IMDSPDevice2 Interface</a>
 

 

