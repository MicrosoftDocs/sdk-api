---
UID: NF:mswmdm.IMDSPDevice.GetFormatSupport
title: IMDSPDevice::GetFormatSupport (mswmdm.h)
description: The GetFormatSupport method retrieves all the formats supported by the device. The format information includes codecs, file formats, and digital rights management schemes.
helpviewer_keywords: ["GetFormatSupport","GetFormatSupport method [windows Media Device Manager]","GetFormatSupport method [windows Media Device Manager]","IMDSPDevice interface","IMDSPDevice interface [windows Media Device Manager]","GetFormatSupport method","IMDSPDevice.GetFormatSupport","IMDSPDevice::GetFormatSupport","IMDSPDeviceGetFormatSupport","mswmdm/IMDSPDevice::GetFormatSupport","wmdm.imdspdevice_getformatsupport"]
old-location: wmdm\imdspdevice_getformatsupport.htm
tech.root: WMDM
ms.assetid: ac50ac7d-bd55-4ece-8af8-5c8b2f7736e8
ms.date: 12/05/2018
ms.keywords: GetFormatSupport, GetFormatSupport method [windows Media Device Manager], GetFormatSupport method [windows Media Device Manager],IMDSPDevice interface, IMDSPDevice interface [windows Media Device Manager],GetFormatSupport method, IMDSPDevice.GetFormatSupport, IMDSPDevice::GetFormatSupport, IMDSPDeviceGetFormatSupport, mswmdm/IMDSPDevice::GetFormatSupport, wmdm.imdspdevice_getformatsupport
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
 - IMDSPDevice::GetFormatSupport
 - mswmdm/IMDSPDevice::GetFormatSupport
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
 - IMDSPDevice.GetFormatSupport
---

# IMDSPDevice::GetFormatSupport


## -description

The <b>GetFormatSupport</b> method retrieves all the formats supported by the device. The format information includes codecs, file formats, and digital rights management schemes.

## -parameters

### -param pFormatEx [out]

Pointer to an array of <a href="/windows/desktop/WMDM/-waveformatex">_WAVEFORMATEX</a> structures containing information about codecs and bit rates supported by the device.

### -param pnFormatCount [out]

Pointer to the number of elements in the <i>pFormatEx</i> array.

### -param pppwszMimeType [out]

Pointer to an array that describes file formats and digital rights management schemes supported by the device.

### -param pnMimeTypeCount [out]

Pointer to the number of elements in the <i>pppwszMimeType</i> array.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Memory for the <i>pFormatEx</i> and <i>pppwszMimeType</i> parameters is allocated by this method and must be freed by the caller using <b>CoTaskMemFree</b>, a standard Win32 function.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice Interface</a>