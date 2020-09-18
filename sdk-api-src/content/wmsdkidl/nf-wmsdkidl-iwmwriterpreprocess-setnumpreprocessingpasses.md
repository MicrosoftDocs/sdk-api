---
UID: NF:wmsdkidl.IWMWriterPreprocess.SetNumPreprocessingPasses
title: IWMWriterPreprocess::SetNumPreprocessingPasses (wmsdkidl.h)
description: The SetNumPreprocessingPasses method sets the number of passes to perform on an input.
helpviewer_keywords: ["IWMWriterPreprocess interface [windows Media Format]","SetNumPreprocessingPasses method","IWMWriterPreprocess.SetNumPreprocessingPasses","IWMWriterPreprocess::SetNumPreprocessingPasses","IWMWriterPreprocessSetNumPreprocessingPasses","SetNumPreprocessingPasses","SetNumPreprocessingPasses method [windows Media Format]","SetNumPreprocessingPasses method [windows Media Format]","IWMWriterPreprocess interface","wmformat.iwmwriterpreprocess_setnumpreprocessingpasses","wmsdkidl/IWMWriterPreprocess::SetNumPreprocessingPasses"]
old-location: wmformat\iwmwriterpreprocess_setnumpreprocessingpasses.htm
tech.root: wmformat
ms.assetid: 81ff36e1-cce5-4c99-bf3a-ee2f1050c026
ms.date: 12/05/2018
ms.keywords: IWMWriterPreprocess interface [windows Media Format],SetNumPreprocessingPasses method, IWMWriterPreprocess.SetNumPreprocessingPasses, IWMWriterPreprocess::SetNumPreprocessingPasses, IWMWriterPreprocessSetNumPreprocessingPasses, SetNumPreprocessingPasses, SetNumPreprocessingPasses method [windows Media Format], SetNumPreprocessingPasses method [windows Media Format],IWMWriterPreprocess interface, wmformat.iwmwriterpreprocess_setnumpreprocessingpasses, wmsdkidl/IWMWriterPreprocess::SetNumPreprocessingPasses
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
 - IWMWriterPreprocess::SetNumPreprocessingPasses
 - wmsdkidl/IWMWriterPreprocess::SetNumPreprocessingPasses
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
 - IWMWriterPreprocess.SetNumPreprocessingPasses
---

# IWMWriterPreprocess::SetNumPreprocessingPasses


## -description

The <b>SetNumPreprocessingPasses</b> method sets the number of passes to perform on an input.

## -parameters

### -param dwInputNum [in]

<b>DWORD</b> containing the input number for which you want to set the number of passes.

### -param dwFlags [in]

Reserved. Set to zero.

### -param dwNumPasses [in]

<b>DWORD</b> containing the number of preprocessing passes.

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
<i>dwNumPasses</i> is zero.

OR

<i>dwInputNum</i> specifies an invalid input stream.

OR

<i>dwNumPasses</i> is greater than the maximum number of passes allowed for the specified input.

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

The preprocessor has already been configured.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess">IWMWriterPreprocess Interface</a>