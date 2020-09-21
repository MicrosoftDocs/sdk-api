---
UID: NF:mswmdm.IMDSPDevice2.GetFormatSupport2
title: IMDSPDevice2::GetFormatSupport2 (mswmdm.h)
description: The GetFormatSupport2 method gets the formats supported by a device, including audio and video codecs, and MIME file formats.
helpviewer_keywords: ["GetFormatSupport2","GetFormatSupport2 method [windows Media Device Manager]","GetFormatSupport2 method [windows Media Device Manager]","IMDSPDevice2 interface","IMDSPDevice2 interface [windows Media Device Manager]","GetFormatSupport2 method","IMDSPDevice2.GetFormatSupport2","IMDSPDevice2::GetFormatSupport2","IMDSPDevice2GetFormatSupport2","mswmdm/IMDSPDevice2::GetFormatSupport2","wmdm.imdspdevice2_getformatsupport2"]
old-location: wmdm\imdspdevice2_getformatsupport2.htm
tech.root: WMDM
ms.assetid: 2b05575b-5a43-4c12-a216-1b9f55742b6c
ms.date: 12/05/2018
ms.keywords: GetFormatSupport2, GetFormatSupport2 method [windows Media Device Manager], GetFormatSupport2 method [windows Media Device Manager],IMDSPDevice2 interface, IMDSPDevice2 interface [windows Media Device Manager],GetFormatSupport2 method, IMDSPDevice2.GetFormatSupport2, IMDSPDevice2::GetFormatSupport2, IMDSPDevice2GetFormatSupport2, mswmdm/IMDSPDevice2::GetFormatSupport2, wmdm.imdspdevice2_getformatsupport2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDSPDevice2::GetFormatSupport2
 - mswmdm/IMDSPDevice2::GetFormatSupport2
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
 - IMDSPDevice2.GetFormatSupport2
---

# IMDSPDevice2::GetFormatSupport2


## -description

The <b>GetFormatSupport2</b> method gets the formats supported by a device, including audio and video codecs, and MIME file formats.

## -parameters

### -param dwFlags [in]

<b>DWORD</b> containing audio formats, video formats, and MIME types. This flag specifies what the application is requesting the service provider to fill in. The caller can set one or more of the following three values.

<table>
<tr>
<th>Value
                </th>
<th>Description
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

Pointer to an array of <a href="/windows/desktop/WMDM/-waveformatex">_WAVEFORMATEX</a> structures containing information about audio codecs and bit rates supported by the device.

### -param pnAudioFormatCount [out]

Pointer to an integer containing the audio format count.

### -param ppVideoFormatEx [out]

Pointer to an array of <a href="/windows/desktop/WMDM/-videoinfoheader">_VIDEOINFOHEADER</a> structures containing information about video codecs and formats supported by the device.

### -param pnVideoFormatCount [out]

Pointer to an integer containing the video format count.

### -param ppFileType [out]

Pointer to an array of <a href="/windows/desktop/WMDM/wmfilecapabilities">WMFILECAPABILITIES</a> structures containing information about file types supported by the device.

### -param pnFileTypeCount [out]

Pointer to an integer containing the file format count.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2">IMDSPDevice2 Interface</a>