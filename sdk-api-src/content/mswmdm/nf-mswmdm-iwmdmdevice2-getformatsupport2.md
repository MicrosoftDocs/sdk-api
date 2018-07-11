---
UID: NF:mswmdm.IWMDMDevice2.GetFormatSupport2
title: IWMDMDevice2::GetFormatSupport2
author: windows-sdk-content
description: The GetFormatSupport2 method retrieves the formats supported by the device, including audio and video codecs, and MIME file formats.
old-location: wmdm\iwmdmdevice2_getformatsupport2.htm
old-project: WMDM
ms.assetid: 9ace6192-5b50-40f0-98b4-5cab26a48798
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetFormatSupport2, GetFormatSupport2 method [windows Media Device Manager], GetFormatSupport2 method [windows Media Device Manager],IWMDMDevice2 interface, IWMDMDevice2 interface [windows Media Device Manager],GetFormatSupport2 method, IWMDMDevice2.GetFormatSupport2, IWMDMDevice2::GetFormatSupport2, IWMDMDevice2GetFormatSupport2, mswmdm/IWMDMDevice2::GetFormatSupport2, wmdm.iwmdmdevice2_getformatsupport2
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMDevice2.GetFormatSupport2
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

