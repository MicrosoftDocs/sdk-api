---
UID: NF:wmsdkidl.IWMDRMReader2.GetCopyOutputLevels
title: IWMDRMReader2::GetCopyOutputLevels (wmsdkidl.h)
description: The GetCopyOutputLevels method retrieves the output protection levels (OPLs) that apply to the copy action in the license of the file loaded in the reader.
helpviewer_keywords: ["GetCopyOutputLevels","GetCopyOutputLevels method [windows Media Format]","GetCopyOutputLevels method [windows Media Format]","IWMDRMReader2 interface","IWMDRMReader2 interface [windows Media Format]","GetCopyOutputLevels method","IWMDRMReader2.GetCopyOutputLevels","IWMDRMReader2::GetCopyOutputLevels","IWMDRMReader2GetCopyOutputLevels","wmformat.iwmdrmreader2_getcopyoutputlevels","wmsdkidl/IWMDRMReader2::GetCopyOutputLevels"]
old-location: wmformat\iwmdrmreader2_getcopyoutputlevels.htm
tech.root: wmformat
ms.assetid: 32c8110b-1a96-432d-a82c-5769757dd4f6
ms.date: 4/26/2023
ms.keywords: GetCopyOutputLevels, GetCopyOutputLevels method [windows Media Format], GetCopyOutputLevels method [windows Media Format],IWMDRMReader2 interface, IWMDRMReader2 interface [windows Media Format],GetCopyOutputLevels method, IWMDRMReader2.GetCopyOutputLevels, IWMDRMReader2::GetCopyOutputLevels, IWMDRMReader2GetCopyOutputLevels, wmformat.iwmdrmreader2_getcopyoutputlevels, wmsdkidl/IWMDRMReader2::GetCopyOutputLevels
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDRMReader2::GetCopyOutputLevels
 - wmsdkidl/IWMDRMReader2::GetCopyOutputLevels
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
 - IWMDRMReader2.GetCopyOutputLevels
---

# IWMDRMReader2::GetCopyOutputLevels


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>GetCopyOutputLevels</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>GetCopyOutputLevels</b> method retrieves the output protection levels (OPLs) that apply to the copy action in the license of the file loaded in the reader.

## -parameters

### -param pCopyOPL [out]

Address of a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl">DRM_COPY_OPL</a> structure that receives the output protection levels that apply to copying content. Additional data is appended to the structure. If you pass <b>NULL</b>, the method returns the size of the structure in <i>pcbLength</i>.

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

Before you call this method, you must call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses">SetEvaluateOutputLevelLicenses</a> to configure the reader to evaluate licenses that contain output protection levels.

If the OPL information returned by this method indicates that you cannot copy the content using the desired technology, you can call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense">TryNextLicense</a> to find out whether there is another license on the computer that you can use.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2">IWMDRMReader2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels">IWMDRMReader2::GetPlayOutputLevels</a>