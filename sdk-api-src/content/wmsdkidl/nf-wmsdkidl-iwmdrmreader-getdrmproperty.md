---
UID: NF:wmsdkidl.IWMDRMReader.GetDRMProperty
title: IWMDRMReader::GetDRMProperty (wmsdkidl.h)
description: The GetDRMProperty method retrieves DRM-specific file attributes and run-time properties.
helpviewer_keywords: ["GetDRMProperty","GetDRMProperty method [windows Media Format]","GetDRMProperty method [windows Media Format]","IWMDRMReader interface","IWMDRMReader interface [windows Media Format]","GetDRMProperty method","IWMDRMReader.GetDRMProperty","IWMDRMReader::GetDRMProperty","IWMDRMReaderGetDRMProperty","wmformat.iwmdrmreader_getdrmproperty","wmsdkidl/IWMDRMReader::GetDRMProperty"]
old-location: wmformat\iwmdrmreader_getdrmproperty.htm
tech.root: wmformat
ms.assetid: 86ee18be-38a9-4f76-810c-e33281df8c23
ms.date: 4/26/2023
ms.keywords: GetDRMProperty, GetDRMProperty method [windows Media Format], GetDRMProperty method [windows Media Format],IWMDRMReader interface, IWMDRMReader interface [windows Media Format],GetDRMProperty method, IWMDRMReader.GetDRMProperty, IWMDRMReader::GetDRMProperty, IWMDRMReaderGetDRMProperty, wmformat.iwmdrmreader_getdrmproperty, wmsdkidl/IWMDRMReader::GetDRMProperty
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDRMReader::GetDRMProperty
 - wmsdkidl/IWMDRMReader::GetDRMProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMDRMReader.GetDRMProperty
---

# IWMDRMReader::GetDRMProperty


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>GetDRMProperty</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>GetDRMProperty</b> method retrieves DRM-specific file attributes and run-time properties.

## -parameters

### -param pwstrName [in]

Specifies the property or file attribute to retrieve.

### -param pdwType [out]

Pointer that receives the data type of the returned value.

### -param pValue [out]

Pointer to the value requested in <i>pwstrName</i>.

### -param pcbLength [out]

Size of <i>pValue</i>, in bytes.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method can be used to retrieve both DRM header attributes and DRM license information for the current file. DRM-related constants are defined in drmexternals.idl and wmsdkidl.idl.

If you specify a "license state" constant, the returned data is a pointer to a <a href="/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)">WM_LICENSE_STATE_DATA</a> structure that fully describes the terms of the license for the particular right. The supported license state constants are described in the following table.

<table>
<tr>
<th>Constant
            </th>
<th>Literal string value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>g_wszWMDRM_LicenseState_CollaborativePlay</td>
<td>"LicenseStateData.CollaborativePlay"</td>
<td>License restrictions on playing the file as part of a collaborative peer-to-peer networking scenario.</td>
</tr>
<tr>
<td>g_wszWMDRM_LicenseState_Copy</td>
<td>"LicenseStateData.Copy"</td>
<td>License restrictions on copying the file to a device.</td>
</tr>
<tr>
<td>g_wszWMDRM_LicenseState_CopyToCD</td>
<td>"LicenseStateData.Print.redbook"</td>
<td>License restrictions on copying the file to CD.For DRM version 10 licenses, use g_wszWMDRM_LicenseState_Copy for all copy actions.

</td>
</tr>
<tr>
<td>g_wszWMDRM_LicenseState_CopyToNonSDMIDevice</td>
<td>"LicenseStateData.Transfer.NONSDMI"</td>
<td>License restrictions on copying the file to a non-SMDI device.For DRM version 10 licenses, use g_wszWMDRM_LicenseState_Copy for all copy actions.

</td>
</tr>
<tr>
<td>g_wszWMDRM_LicenseState_CopyToSDMIDevice</td>
<td>"LicenseStateData.Transfer.SDMI"</td>
<td>License restrictions on copying the file to an <a href="/windows/desktop/wmformat/wmformat-glossary">SDMI</a> device.For DRM version 10 licenses, use g_wszWMDRM_LicenseState_Copy for all copy actions.

</td>
</tr>
<tr>
<td>g_wszWMDRM_LicenseState_Playback</td>
<td>"LicenseStateData.Play"</td>
<td>License restrictions on playing the file.</td>
</tr>
<tr>
<td>g_wszWMDRM_LicenseState_PlaylistBurn</td>
<td>"LicenseStateData.PlaylistBurn"</td>
<td>License restrictions on copying the file to Red Book audio CD as part of a playlist.</td>
</tr>
</table>
 

If you specify an "action allowed" constant, the returned data is a Boolean that indicates whether a specified action is allowed at this time. The supported constants are:

<table>
<tr>
<th>Constant
            </th>
<th>Literal string value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>g_wszWMDRM_ActionAllowed_Backup</td>
<td>"ActionAllowed.Backup"</td>
<td>Right to back up the file now.</td>
</tr>
<tr>
<td>g_wszWMDRM_ActionAllowed_CollaborativePlay</td>
<td>"ActionAllowed.CollaborativePlay"</td>
<td>Right to play the file as part of a collaborative peer-to-peer networking scenario.</td>
</tr>
<tr>
<td>g_wszWMDRM_ActionAllowed_Copy</td>
<td>"ActionAllowed.Copy"</td>
<td>Right to copy the file to a device.</td>
</tr>
<tr>
<td>g_wszWMDRM_ActionAllowed_CopyToCD</td>
<td>"ActionAllowed.Print.redbook"</td>
<td>Right to copy file to CD.For DRM version 10 licenses, check g_wszWMDRM_ActionAllowed_Copy for all copy actions.

</td>
</tr>
<tr>
<td>g_wszWMDRM_ActionAllowed_CopyToSDMIDevice</td>
<td>"ActionAllowed.Transfer.SDMI"</td>
<td>Right to copy file to an SDMI device.For DRM version 10 licenses, check g_wszWMDRM_ActionAllowed_Copy for all copy actions.

</td>
</tr>
<tr>
<td>g_wszWMDRM_ActionAllowed_CopyToNonSDMIDevice</td>
<td>"ActionAllowed.Transfer.NONSDMI"</td>
<td>Right to copy file to a non-SMDI device.For DRM version 10 licenses, check g_wszWMDRM_ActionAllowed_Copy for all copy actions.

</td>
</tr>
<tr>
<td>g_wszWMDRM_ActionAllowed_Playback</td>
<td>"ActionAllowed.Play"</td>
<td>Right to play file.</td>
</tr>
<tr>
<td>g_wszWMDRM_ActionAllowed_PlaylistBurn</td>
<td>"ActionAllowed.PlaylistBurn"</td>
<td>Right to copy the file to Red Book audio CD as part of a playlist.</td>
</tr>
</table>
 

If you specify a "DRM Header" constant, the returned value is the string literal for the specified property. The supported DRM Header constants are:

<table>
<tr>
<th>Constant
            </th>
<th>Literal string value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>g_wszWMDRM_DRMHeader_KeyID</td>
<td>"DRMHeader.KID"</td>
<td>DRM key value.</td>
</tr>
<tr>
<td>g_wszWMDRM_DRMHeader_LicenseAcqURL</td>
<td>"DRMHeader.LAINFO"</td>
<td>DRM license acquisition URL.</td>
</tr>
<tr>
<td>g_wszWMDRM_DRMHeader_ContentID</td>
<td>"DRMHeader.CID"</td>
<td>DRM content ID.</td>
</tr>
<tr>
<td>g_wszWMDRM_DRMHeader_IndividualizedVersion</td>
<td>"DRMHeader.SECURITYVERSION"</td>
<td>Individualized version.</td>
</tr>
<tr>
<td>g_wszWMDRM_DRMHeader_ContentDistributor</td>
<td>"DRMHeader.ContentDistributor"</td>
<td>Content distributor.</td>
</tr>
<tr>
<td>g_wszWMDRM_DRMHeader_SubscriptionContentID</td>
<td>"DRMHeader.SubscriptionContentID"</td>
<td>Subscription content ID.</td>
</tr>
</table>
 

Before calling this method on a new file, always call the helper function <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmiscontentprotected">WMIsContentProtected</a> to ensure that the file is protected with DRM. It is important to do this because in some cases this method might succeed when called on unprotected content.

## -see-also

<a href="/windows/desktop/wmformat/drm-attribute-list">DRM Attribute List</a>



<a href="/windows/desktop/wmformat/drm-properties">DRM Properties</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty">IWMDRMEditor::GetDRMProperty</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty">IWMDRMReader::SetDRMProperty</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a>