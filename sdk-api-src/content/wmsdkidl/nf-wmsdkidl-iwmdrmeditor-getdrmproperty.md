---
UID: NF:wmsdkidl.IWMDRMEditor.GetDRMProperty
title: IWMDRMEditor::GetDRMProperty
author: windows-sdk-content
description: The GetDRMProperty method retrieves the specified DRM property.
old-location: wmformat\iwmdrmeditor_getdrmproperty.htm
old-project: wmformat
ms.assetid: b0a7b07d-f0c0-4715-a9c3-7babf3bf7af9
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetDRMProperty, GetDRMProperty method [windows Media Format], GetDRMProperty method [windows Media Format],IWMDRMEditor interface, IWMDRMEditor interface [windows Media Format],GetDRMProperty method, IWMDRMEditor.GetDRMProperty, IWMDRMEditor::GetDRMProperty, IWMDRMEditorGetDRMProperty, wmformat.iwmdrmeditor_getdrmproperty, wmsdkidl/IWMDRMEditor::GetDRMProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMEditor::GetDRMProperty


## -description


<p class="CCE_Message">[<b>GetDRMProperty</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>GetDRMProperty</b> method retrieves the specified <a href="https://docs.microsoft.com/windows/desktop//wmformat/wmformat-glossary">DRM</a> property.




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



This method retrieves only DRM properties listed below. The file must first be opened using <a href="https://msdn.microsoft.com/01dd09ff-35d2-4e00-9eab-5110a426449f">IWMMetadataEditor::Open</a> or <a href="https://msdn.microsoft.com/e35f5f85-659e-4a1f-8bfd-4ad3e946d733">IWMMetadataEditor2::OpenEx</a>.

Also, before calling <b>GetDRMProperty</b> on an opened file, always call the helper function <a href="https://msdn.microsoft.com/a28cdf06-8c4f-41ff-b9dc-eddf9bc9d674">WMIsContentProtected</a> to ensure that the file is protected with DRM. It is important to do this because in some cases this method might succeed when called on unprotected content.

The following properties are accessible from this method:

<ul>
<li>
<a href="https://msdn.microsoft.com/1d728135-25e9-4ab8-873d-b7df3e8cae83">DRM_IsDRM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/868e3ada-d608-41d6-93d7-0b7930cbf2f9">DRM_IsDRMCached</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9acaac44-81b2-467c-9510-023fbb47dd04">DRM_BaseLicenseAcqURL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fbf62e8d-069e-427b-9093-6c579cdaa96a">DRM_Rights</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d5967f5b-99b6-41ea-8494-ac4a7331bbfe">DRM_LicenseID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7c8d7631-7edc-482d-afdb-758c4a0ecc22">DRM_ActionAllowed_Playback</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c650bb2e-6cec-404a-8ece-7a5687cda99f">DRM_ActionAllowed_CopyToCD</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3ffb9c8f-5640-4ab5-9939-f9525ab960c6">DRM_ActionAllowed_CopyToSDMIDevice</a>
</li>
<li>
<a href="https://msdn.microsoft.com/517ceeb5-4979-4667-ba54-8b9b1c6069f2">DRM_ActionAllowed_CopyToNonSDMIDevice</a>
</li>
<li>
<a href="https://msdn.microsoft.com/49b503ff-a2ca-405c-a8ac-49653c62e13e">DRM_ActionAllowed_Backup</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cf9fe829-8473-4dd5-9a99-48b709fec0d8">DRM_DRMHeader_KeyID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/00c788b4-b291-4df5-9926-0badc7357faf">DRM_DRMHeader_LicenseAcqURL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fda38778-2fdf-4218-aad2-e4cf351d74e9">DRM_DRMHeader_ContentID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c">DRM_DRMHeader_IndividualizedVersion</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ea9ae7ba-35cc-4e86-995c-9abcdae48f9c">DRM_DRMHeader_ContentDistributor</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e582d841-4865-40d3-889e-847d3aac0a7c">DRM_DRMHeader_SubscriptionContentID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/deb559e6-1854-4ac7-bc77-c641e9579fde">DRM_LicenseState_Playback</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0a32ce53-87ce-4b63-bfd6-3a0dd629dabc">DRM_LicenseState_CopyToCD</a>
</li>
<li>
<a href="https://msdn.microsoft.com/16d6748f-7998-4239-925d-d9d3952aab1b">DRM_LicenseState_CopyToSDMIDevice</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aa0099b0-c6f8-4e27-a1f4-b98155d277aa">DRM_LicenseState_CopyToNonSDMIDevice</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/222ef91c-b776-4de8-b1ad-88c2beca05aa">DRM Attribute List</a>



<a href="https://msdn.microsoft.com/862fc8bc-6e40-4496-862a-c12c8a382116">DRM Properties</a>



<a href="https://msdn.microsoft.com/a404d30d-0b42-44c9-93e6-3eb9ef9e40fc">IWMDRMEditor Interface</a>
 

 

