---
UID: NF:wmcontainer.IMFASFContentInfo.GetProfile
title: IMFASFContentInfo::GetProfile (wmcontainer.h)
author: windows-sdk-content
description: Retrieves an Advanced Systems Format (ASF) profile that describes the ASF content.
old-location: mf\imfasfcontentinfo_getprofile.htm
tech.root: medfound
ms.assetid: 6f74c896-a0c0-407b-b893-de15863bc2eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 6f74c896-a0c0-407b-b893-de15863bc2eb, GetProfile, GetProfile method [Media Foundation], GetProfile method [Media Foundation],IMFASFContentInfo interface, IMFASFContentInfo interface [Media Foundation],GetProfile method, IMFASFContentInfo.GetProfile, IMFASFContentInfo::GetProfile, mf.imfasfcontentinfo_getprofile, wmcontainer/IMFASFContentInfo::GetProfile
ms.topic: method
f1_keywords: 
 - "wmcontainer/IMFASFContentInfo.GetProfile"
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFContentInfo.GetProfile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFASFContentInfo::GetProfile


## -description



Retrieves an Advanced Systems Format (ASF) profile that describes the ASF content.




## -parameters




### -param ppIProfile [out]

Receives an <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a> interface pointer. The caller must release the interface. If the object does not have an ASF profile, this parameter receives the value <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The profile is set by calling either <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile">IMFASFContentInfo::SetProfile</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader">IMFASFContentInfo::ParseHeader</a>.

The ASF profile object returned by this method does not include any of the <b>MF_PD_ASF_xxx</b> attributes (see <a href="https://docs.microsoft.com/windows/desktop/medfound/presentation-descriptor-attributes">Presentation Descriptor Attributes</a>). To get these attributes, do the following:

<ol>
<li>
Call <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor">IMFASFContentInfo::GeneratePresentationDescriptor</a> to get the ASF presentation descriptor. You can query the presentation descriptor for the <b>MF_PD_ASF_xxx</b> attributes.

</li>
<li>
(Optional.) Call <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor">MFCreateASFProfileFromPresentationDescriptor</a> to convert the presentation descriptor into an ASF profile. The profile object created by this function contains the <b>MF_PD_ASF_xxx</b> attributes.

</li>
</ol>
An ASF profile is a template for file encoding, and is intended mainly for creating ASF content. If you are reading an existing ASF file, it is recommended that you use the presentation descriptor to get information about the file. One exception is that the profile contains the mutual exclusion and stream prioritization objects, which are not exposed directly from the presentation descriptor.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/asf-contentinfo-object">ASF ContentInfo Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/initializing-the-contentinfo-object-of-a-new-asf-file">Initializing the ContentInfo Object of a New ASF File</a>
 

 

