---
UID: NF:mswmdm.IMDSPDevice3.GetFormatCapability
title: IMDSPDevice3::GetFormatCapability (mswmdm.h)
description: The GetFormatCapability method retrieves information from a device about the values or ranges of values supported by the device for each aspect of a particular object format.
helpviewer_keywords: ["GetFormatCapability","GetFormatCapability method [windows Media Device Manager]","GetFormatCapability method [windows Media Device Manager]","IMDSPDevice3 interface","IMDSPDevice3 interface [windows Media Device Manager]","GetFormatCapability method","IMDSPDevice3.GetFormatCapability","IMDSPDevice3::GetFormatCapability","IMDSPDevice3GetFormatCapability","mswmdm/IMDSPDevice3::GetFormatCapability","wmdm.imdspdevice3_getformatcapability"]
old-location: wmdm\imdspdevice3_getformatcapability.htm
tech.root: WMDM
ms.assetid: ef53d7d2-dd9c-4705-9a25-9c0b16d03e7e
ms.date: 12/05/2018
ms.keywords: GetFormatCapability, GetFormatCapability method [windows Media Device Manager], GetFormatCapability method [windows Media Device Manager],IMDSPDevice3 interface, IMDSPDevice3 interface [windows Media Device Manager],GetFormatCapability method, IMDSPDevice3.GetFormatCapability, IMDSPDevice3::GetFormatCapability, IMDSPDevice3GetFormatCapability, mswmdm/IMDSPDevice3::GetFormatCapability, wmdm.imdspdevice3_getformatcapability
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
 - IMDSPDevice3::GetFormatCapability
 - mswmdm/IMDSPDevice3::GetFormatCapability
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
 - IMDSPDevice3.GetFormatCapability
---

# IMDSPDevice3::GetFormatCapability


## -description

The <b>GetFormatCapability</b> method retrieves information from a device about the values or ranges of values supported by the device for each aspect of a particular object format.

## -parameters

### -param format [in]

<a href="/windows/desktop/WMDM/wmdm-formatcode">WMDM_FORMATCODE</a>


Enumerated value representing inquired format.

### -param pFormatSupport [out]

Returned <a href="/windows/desktop/WMDM/wmdm-format-capability">WMDM_FORMAT_CAPABILITY</a> structure containing the values or ranges of values supported for each aspect of a particular object format.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method can be called for any of the supported formats. The list of supported formats are represented by <b>g_wszWMDMFormatsSupported</b> device property.

For a particular format, this method should return all configurations of supported properties (for example, combinations of bit rate and sample rate). This information is expressed as a format capability. For detailed information, see <a href="/windows/desktop/WMDM/wmdm-format-capability">WMDM_FORMAT_CAPABILITY</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3">IMDSPDevice3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-getproperty">IMDSPDevice3::GetProperty</a>



<a href="/windows/desktop/WMDM/wmdm-enum-prop-valid-values-form">WMDM_ENUM_PROP_VALID_VALUES_FORM</a>



<a href="/windows/desktop/WMDM/wmdm-format-capability">WMDM_FORMAT_CAPABILITY</a>



<a href="/windows/desktop/WMDM/wmdm-prop-config">WMDM_PROP_CONFIG</a>



<a href="/windows/desktop/WMDM/wmdm-prop-desc">WMDM_PROP_DESC</a>



<a href="/windows/desktop/WMDM/wmdm-prop-values-enum">WMDM_PROP_VALUES_ENUM</a>



<a href="/windows/desktop/WMDM/wmdm-prop-values-range">WMDM_PROP_VALUES_RANGE</a>