---
UID: NF:wmsdkidl.IWMDRMReader2.GetCopyOutputLevels
title: IWMDRMReader2::GetCopyOutputLevels (wmsdkidl.h)
description: The GetCopyOutputLevels method retrieves the output protection levels (OPLs) that apply to the copy action in the license of the file loaded in the reader.
helpviewer_keywords: ["GetCopyOutputLevels","GetCopyOutputLevels method [windows Media Format]","GetCopyOutputLevels method [windows Media Format]","IWMDRMReader2 interface","IWMDRMReader2 interface [windows Media Format]","GetCopyOutputLevels method","IWMDRMReader2.GetCopyOutputLevels","IWMDRMReader2::GetCopyOutputLevels","IWMDRMReader2GetCopyOutputLevels","wmformat.iwmdrmreader2_getcopyoutputlevels","wmsdkidl/IWMDRMReader2::GetCopyOutputLevels"]
old-location: wmformat\iwmdrmreader2_getcopyoutputlevels.htm
tech.root: wmformat
ms.assetid: 32c8110b-1a96-432d-a82c-5769757dd4f6
ms.date: 12/05/2018
ms.keywords: GetCopyOutputLevels, GetCopyOutputLevels method [windows Media Format], GetCopyOutputLevels method [windows Media Format],IWMDRMReader2 interface, IWMDRMReader2 interface [windows Media Format],GetCopyOutputLevels method, IWMDRMReader2.GetCopyOutputLevels, IWMDRMReader2::GetCopyOutputLevels, IWMDRMReader2GetCopyOutputLevels, wmformat.iwmdrmreader2_getcopyoutputlevels, wmsdkidl/IWMDRMReader2::GetCopyOutputLevels
f1_keywords:
- wmsdkidl/IWMDRMReader2.GetCopyOutputLevels
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- WMStubDRM.lib
- WMStubDRM.dll
api_name:
- IWMDRMReader2.GetCopyOutputLevels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDRMReader2::GetCopyOutputLevels


## -description


<p class="CCE_Message">[<b>GetCopyOutputLevels</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>GetCopyOutputLevels</b> method retrieves the output protection levels (OPLs) that apply to the copy action in the license of the file loaded in the reader.




## -parameters




### -param pCopyOPL [out]

Address of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl">DRM_COPY_OPL</a> structure that receives the output protection levels that apply to copying content. Additional data is appended to the structure. If you pass <b>NULL</b>, the method returns the size of the structure in <i>pcbLength</i>.


### -param pcbLength [in, out]

Address of a variable that contains the size of the <b>DRM_COPY_OPL</b> structure in bytes. On input set to the size of the allocated buffer. On return the method sets this value to the size of the structure and any appended data.


### -param pdwMinAppComplianceLevel [out]

Address of a variable that receives the minimum application compliance level.


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



When reading DRM-protected content, you must verify that the destination of the protected content is allowed by the license. Calling this method enables you to check the output protection level required by the license.

Before you call this method, you must call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses">SetEvaluateOutputLevelLicenses</a> to configure the reader to evaluate licenses that contain output protection levels.

If the OPL information returned by this method indicates that you cannot copy the content using the desired technology, you can call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense">TryNextLicense</a> to find out whether there is another license on the computer that you can use.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2">IWMDRMReader2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels">IWMDRMReader2::GetPlayOutputLevels</a>
 

 

