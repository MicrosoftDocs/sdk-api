---
UID: NF:dshowasf.IConfigAsfWriter.ConfigureFilterUsingProfileId
title: IConfigAsfWriter::ConfigureFilterUsingProfileId (dshowasf.h)
description: The ConfigureFilterUsingProfileId method sets a Windows Media Format 4.0 profile on the WM ASF Writer filter. This method is deprecated. Applications should use the IConfigAsfWriter::ConfigureFilterUsingProfile method to set the profile.
helpviewer_keywords: ["ConfigureFilterUsingProfileId","ConfigureFilterUsingProfileId method [DirectShow]","ConfigureFilterUsingProfileId method [DirectShow]","IConfigAsfWriter interface","IConfigAsfWriter interface [DirectShow]","ConfigureFilterUsingProfileId method","IConfigAsfWriter.ConfigureFilterUsingProfileId","IConfigAsfWriter::ConfigureFilterUsingProfileId","IConfigAsfWriterConfigureFilterUsingProfileId","dshow.iconfigasfwriter_configurefilterusingprofileid","dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfileId"]
old-location: dshow\iconfigasfwriter_configurefilterusingprofileid.htm
tech.root: dshow
ms.assetid: e532001a-e2ff-4ad4-8fef-2fa5b051d1f5
ms.date: 12/05/2018
ms.keywords: ConfigureFilterUsingProfileId, ConfigureFilterUsingProfileId method [DirectShow], ConfigureFilterUsingProfileId method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],ConfigureFilterUsingProfileId method, IConfigAsfWriter.ConfigureFilterUsingProfileId, IConfigAsfWriter::ConfigureFilterUsingProfileId, IConfigAsfWriterConfigureFilterUsingProfileId, dshow.iconfigasfwriter_configurefilterusingprofileid, dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfileId
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConfigAsfWriter::ConfigureFilterUsingProfileId
 - dshowasf/IConfigAsfWriter::ConfigureFilterUsingProfileId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter.ConfigureFilterUsingProfileId
---

# IConfigAsfWriter::ConfigureFilterUsingProfileId


## -description

The <code>ConfigureFilterUsingProfileId</code> method sets a Windows Media Format 4.0 profile on the <a href="/windows/desktop/DirectShow/wm-asf-writer-filter">WM ASF Writer</a> filter. This method is deprecated. Applications should use the <a href="/windows/desktop/api/dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile">IConfigAsfWriter::ConfigureFilterUsingProfile</a> method to set the profile.

## -parameters

### -param dwProfileId [in]

Profile ID as defined in version 4.0 of the Windows Media Format SDK.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The profile is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is stopped.

</td>
</tr>
</table>

## -remarks

This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter Interface</a>