---
UID: NF:wmsdkidl.IWMDRMReader2.SetEvaluateOutputLevelLicenses
title: IWMDRMReader2::SetEvaluateOutputLevelLicenses (wmsdkidl.h)
description: The SetEvaluateOutputLevelLicenses method sets the reader to evaluate licenses that use output protection levels (OPLs).
helpviewer_keywords: ["IWMDRMReader2 interface [windows Media Format]","SetEvaluateOutputLevelLicenses method","IWMDRMReader2.SetEvaluateOutputLevelLicenses","IWMDRMReader2::SetEvaluateOutputLevelLicenses","IWMDRMReader2SetEvaluateOutputLevelLicenses","SetEvaluateOutputLevelLicenses","SetEvaluateOutputLevelLicenses method [windows Media Format]","SetEvaluateOutputLevelLicenses method [windows Media Format]","IWMDRMReader2 interface","wmformat.iwmdrmreader2_setevaluateoutputlevellicenses","wmsdkidl/IWMDRMReader2::SetEvaluateOutputLevelLicenses"]
old-location: wmformat\iwmdrmreader2_setevaluateoutputlevellicenses.htm
tech.root: wmformat
ms.assetid: 5a146ec4-a733-483c-8b08-2bee0081bd96
ms.date: 4/26/2023
ms.keywords: IWMDRMReader2 interface [windows Media Format],SetEvaluateOutputLevelLicenses method, IWMDRMReader2.SetEvaluateOutputLevelLicenses, IWMDRMReader2::SetEvaluateOutputLevelLicenses, IWMDRMReader2SetEvaluateOutputLevelLicenses, SetEvaluateOutputLevelLicenses, SetEvaluateOutputLevelLicenses method [windows Media Format], SetEvaluateOutputLevelLicenses method [windows Media Format],IWMDRMReader2 interface, wmformat.iwmdrmreader2_setevaluateoutputlevellicenses, wmsdkidl/IWMDRMReader2::SetEvaluateOutputLevelLicenses
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
 - IWMDRMReader2::SetEvaluateOutputLevelLicenses
 - wmsdkidl/IWMDRMReader2::SetEvaluateOutputLevelLicenses
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
 - IWMDRMReader2.SetEvaluateOutputLevelLicenses
---

# IWMDRMReader2::SetEvaluateOutputLevelLicenses


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>SetEvaluateOutputLevelLicenses</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>SetEvaluateOutputLevelLicenses</b> method sets the reader to evaluate licenses that use output protection levels (OPLs).

## -parameters

### -param fEvaluate [in]

Flag specifying whether to handle files with licenses that use output protection levels.

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

If your application supports reading DRM-protected files with licenses that use output protection levels, you must call this method and set <i>fEvaluate</i> to <b>TRUE</b>. The call must be made before opening the file.

When a file is opened with OPL support enabled, you must call either <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels">GetCopyOutputLevels</a> or <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels">GetPlayOutputLevels</a>, depending on the actions your application performs. These methods provide minimum OPLs for the associated action.

If you do not call this method, the reader object will not open DRM-protected files that have licenses specifying output protection levels.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2">IWMDRMReader2 Interface</a>