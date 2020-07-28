---
UID: NF:wmsdkidl.IWMDRMEditor.GetDRMProperty
title: IWMDRMEditor::GetDRMProperty (wmsdkidl.h)
description: The GetDRMProperty method retrieves the specified DRM property.
helpviewer_keywords: ["GetDRMProperty","GetDRMProperty method [windows Media Format]","GetDRMProperty method [windows Media Format]","IWMDRMEditor interface","IWMDRMEditor interface [windows Media Format]","GetDRMProperty method","IWMDRMEditor.GetDRMProperty","IWMDRMEditor::GetDRMProperty","IWMDRMEditorGetDRMProperty","wmformat.iwmdrmeditor_getdrmproperty","wmsdkidl/IWMDRMEditor::GetDRMProperty"]
old-location: wmformat\iwmdrmeditor_getdrmproperty.htm
tech.root: wmformat
ms.assetid: b0a7b07d-f0c0-4715-a9c3-7babf3bf7af9
ms.date: 12/05/2018
ms.keywords: GetDRMProperty, GetDRMProperty method [windows Media Format], GetDRMProperty method [windows Media Format],IWMDRMEditor interface, IWMDRMEditor interface [windows Media Format],GetDRMProperty method, IWMDRMEditor.GetDRMProperty, IWMDRMEditor::GetDRMProperty, IWMDRMEditorGetDRMProperty, wmformat.iwmdrmeditor_getdrmproperty, wmsdkidl/IWMDRMEditor::GetDRMProperty
f1_keywords:
- wmsdkidl/IWMDRMEditor.GetDRMProperty
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmvcore.lib
- Wmvcore.dll
- WMStubDRM.lib
- WMStubDRM.dll
api_name:
- IWMDRMEditor.GetDRMProperty
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDRMEditor::GetDRMProperty


## -description


<p class="CCE_Message">[<b>GetDRMProperty</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>GetDRMProperty</b> method retrieves the specified <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">DRM</a> property.




## -parameters




### -param pwstrName [in]

Specifies the DRM file attribute to retrieve.


### -param pdwType [out]

Pointer that receives the data type of the returned value.


### -param pValue [out]

Pointer to the value requested in <i>pwstrName</i>.


### -param pcbLength [out]

Length of <i>pValue</i> in bytes.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method retrieves only DRM properties listed below. The file must first be opened using <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmetadataeditor-open">IWMMetadataEditor::Open</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmetadataeditor2-openex">IWMMetadataEditor2::OpenEx</a>.

Also, before calling <b>GetDRMProperty</b> on an opened file, always call the helper function <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmiscontentprotected">WMIsContentProtected</a> to ensure that the file is protected with DRM. It is important to do this because in some cases this method might succeed when called on unprotected content.

The following properties are accessible from this method:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-isdrm">DRM_IsDRM</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-isdrmcached">DRM_IsDRMCached</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-baselicenseacqurl">DRM_BaseLicenseAcqURL</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-rights">DRM_Rights</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-licenseid">DRM_LicenseID</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-actionallowed-playback">DRM_ActionAllowed_Playback</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-actionallowed-copytocd">DRM_ActionAllowed_CopyToCD</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-actionallowed-copytosdmidevice">DRM_ActionAllowed_CopyToSDMIDevice</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-actionallowed-copytononsdmidevice">DRM_ActionAllowed_CopyToNonSDMIDevice</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-actionallowed-backup">DRM_ActionAllowed_Backup</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-drmheader-keyid">DRM_DRMHeader_KeyID</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-drmheader-licenseacqurl">DRM_DRMHeader_LicenseAcqURL</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-drmheader-contentid">DRM_DRMHeader_ContentID</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-drmheader-individualizedversion">DRM_DRMHeader_IndividualizedVersion</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-drmheader-contentdistributor">DRM_DRMHeader_ContentDistributor</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-drmheader-subscriptioncontentid">DRM_DRMHeader_SubscriptionContentID</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-licensestate-playback">DRM_LicenseState_Playback</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-licensestate-copytocd">DRM_LicenseState_CopyToCD</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-licensestate-copytosdmidevice">DRM_LicenseState_CopyToSDMIDevice</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-licensestate-copytononsdmidevice">DRM_LicenseState_CopyToNonSDMIDevice</a>
</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-attribute-list">DRM Attribute List</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-properties">DRM Properties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor">IWMDRMEditor Interface</a>
 

 

