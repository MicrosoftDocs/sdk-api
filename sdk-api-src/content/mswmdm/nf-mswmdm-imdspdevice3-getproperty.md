---
UID: NF:mswmdm.IMDSPDevice3.GetProperty
title: IMDSPDevice3::GetProperty (mswmdm.h)
description: The GetProperty method retrieves a specific device property.
helpviewer_keywords: ["GetProperty","GetProperty method [windows Media Device Manager]","GetProperty method [windows Media Device Manager]","IMDSPDevice3 interface","IMDSPDevice3 interface [windows Media Device Manager]","GetProperty method","IMDSPDevice3.GetProperty","IMDSPDevice3::GetProperty","IMDSPDevice3TransferSessionBegin","mswmdm/IMDSPDevice3::GetProperty","wmdm.imdspdevice3_getproperty"]
old-location: wmdm\imdspdevice3_getproperty.htm
tech.root: WMDM
ms.assetid: e0665ba6-361d-488c-9100-68f39855b736
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [windows Media Device Manager], GetProperty method [windows Media Device Manager],IMDSPDevice3 interface, IMDSPDevice3 interface [windows Media Device Manager],GetProperty method, IMDSPDevice3.GetProperty, IMDSPDevice3::GetProperty, IMDSPDevice3TransferSessionBegin, mswmdm/IMDSPDevice3::GetProperty, wmdm.imdspdevice3_getproperty
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
 - IMDSPDevice3::GetProperty
 - mswmdm/IMDSPDevice3::GetProperty
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
 - IMDSPDevice3.GetProperty
---

# IMDSPDevice3::GetProperty


## -description

The <b>GetProperty</b> method retrieves a specific device property.

## -parameters

### -param pwszPropName [in]

Name of property being retrieved from the device.

### -param pValue [out]

Returned value for the property.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The variant that <i>pValue</i> points to is set to an empty <b>PROPVARIANT</b>, that is, its VT is set to VT_EMPTY.

Service provider should set this variant to the appropriate property value for the property <i>pwszPropName</i>.

If <i>pwszPropName</i> is <b>g_wszWMDMSupportedDeviceProperties</b>, service provider should return an array of the supported device properties. In such case, the VT of variant should be VT_BSTR | VT_ARRAY.

For a list of standard device property names, see <a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>.

This method is similar to the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage3-getmetadata">IMDSPStorage3::GetMetadata</a> and <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage4-getspecifiedmetadata">IMDSPStorage4::GetSpecifiedMetadata</a> methods for storages, but this method can get only one property at a time.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3">IMDSPDevice3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-setproperty">IMDSPDevice3::SetProperty</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage3-getmetadata">IMDSPStorage3::GetMetadata</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage4-getspecifiedmetadata">IMDSPStorage4::GetSpecifiedMetadata</a>



<a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>