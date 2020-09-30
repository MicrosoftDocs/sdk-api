---
UID: NF:wmsdkidl.IWMWriterPreprocess.BeginPreprocessingPass
title: IWMWriterPreprocess::BeginPreprocessingPass (wmsdkidl.h)
description: The BeginPreprocessingPass method prepares the writer to begin preprocessing samples for the specified input stream.
helpviewer_keywords: ["BeginPreprocessingPass","BeginPreprocessingPass method [windows Media Format]","BeginPreprocessingPass method [windows Media Format]","IWMWriterPreprocess interface","IWMWriterPreprocess interface [windows Media Format]","BeginPreprocessingPass method","IWMWriterPreprocess.BeginPreprocessingPass","IWMWriterPreprocess::BeginPreprocessingPass","IWMWriterPreprocessBeginPreprocessingPass","wmformat.iwmwriterpreprocess_beginpreprocessingpass","wmsdkidl/IWMWriterPreprocess::BeginPreprocessingPass"]
old-location: wmformat\iwmwriterpreprocess_beginpreprocessingpass.htm
tech.root: wmformat
ms.assetid: 593aaa1f-b0eb-43a0-bf73-e90225c07cdf
ms.date: 12/05/2018
ms.keywords: BeginPreprocessingPass, BeginPreprocessingPass method [windows Media Format], BeginPreprocessingPass method [windows Media Format],IWMWriterPreprocess interface, IWMWriterPreprocess interface [windows Media Format],BeginPreprocessingPass method, IWMWriterPreprocess.BeginPreprocessingPass, IWMWriterPreprocess::BeginPreprocessingPass, IWMWriterPreprocessBeginPreprocessingPass, wmformat.iwmwriterpreprocess_beginpreprocessingpass, wmsdkidl/IWMWriterPreprocess::BeginPreprocessingPass
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMWriterPreprocess::BeginPreprocessingPass
 - wmsdkidl/IWMWriterPreprocess::BeginPreprocessingPass
dev_langs:
 - c++
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
 - IWMWriterPreprocess.BeginPreprocessingPass
---

# IWMWriterPreprocess::BeginPreprocessingPass


## -description

The <b>BeginPreprocessingPass</b> method prepares the writer to begin preprocessing samples for the specified input stream.

## -parameters

### -param dwInputNum [in]

<b>DWORD</b> containing the input number that you want to preprocess.

### -param dwFlags [in]

Reserved. Set to zero.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwInputNum</i> specifies an invalid input number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The writer is not running.

OR

The preprocessor is neither waiting to be run nor stopped in the middle of a pass.

OR

The preprocessor has already made as many passes as specified by <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpreprocess-setnumpreprocessingpasses">SetNumPreprocessingPasses</a>.

OR

The input specified is not supported for preprocessing.

</td>
</tr>
</table>

## -remarks

To successfully call <b>BeginPreprocessingPass</b>, the preprocessor must be set to make at least one preprocessing pass with a call to <b>SetNumPreprocessingPasses</b>.

The writer must be activated by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a> before you can call this method.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess">IWMWriterPreprocess Interface</a>