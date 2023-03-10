---
UID: NF:wmsdkidl.IWMWriterPreprocess.EndPreprocessingPass
title: IWMWriterPreprocess::EndPreprocessingPass (wmsdkidl.h)
description: The EndPreprocessingPass method ends a preprocessing pass started with a call to IWMWriterPreprocess::BeginPreprocessingPass.
helpviewer_keywords: ["EndPreprocessingPass","EndPreprocessingPass method [windows Media Format]","EndPreprocessingPass method [windows Media Format]","IWMWriterPreprocess interface","IWMWriterPreprocess interface [windows Media Format]","EndPreprocessingPass method","IWMWriterPreprocess.EndPreprocessingPass","IWMWriterPreprocess::EndPreprocessingPass","IWMWriterPreprocessEndPreprocessingPass","wmformat.iwmwriterpreprocess_endpreprocessingpass","wmsdkidl/IWMWriterPreprocess::EndPreprocessingPass"]
old-location: wmformat\iwmwriterpreprocess_endpreprocessingpass.htm
tech.root: wmformat
ms.assetid: 04ec12fb-946b-46cc-aa3f-515a86b9a217
ms.date: 12/05/2018
ms.keywords: EndPreprocessingPass, EndPreprocessingPass method [windows Media Format], EndPreprocessingPass method [windows Media Format],IWMWriterPreprocess interface, IWMWriterPreprocess interface [windows Media Format],EndPreprocessingPass method, IWMWriterPreprocess.EndPreprocessingPass, IWMWriterPreprocess::EndPreprocessingPass, IWMWriterPreprocessEndPreprocessingPass, wmformat.iwmwriterpreprocess_endpreprocessingpass, wmsdkidl/IWMWriterPreprocess::EndPreprocessingPass
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
 - IWMWriterPreprocess::EndPreprocessingPass
 - wmsdkidl/IWMWriterPreprocess::EndPreprocessingPass
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
 - IWMWriterPreprocess.EndPreprocessingPass
---

# IWMWriterPreprocess::EndPreprocessingPass


## -description

The <b>EndPreprocessingPass</b> method ends a preprocessing pass started with a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpreprocess-beginpreprocessingpass">IWMWriterPreprocess::BeginPreprocessingPass</a>.

## -parameters

### -param dwInputNum [in]

<b>DWORD</b> containing the input number for which you want to halt preprocessing.

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

The preprocessor is not started for the specified stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was an error ending the preprocessing path.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess">IWMWriterPreprocess Interface</a>