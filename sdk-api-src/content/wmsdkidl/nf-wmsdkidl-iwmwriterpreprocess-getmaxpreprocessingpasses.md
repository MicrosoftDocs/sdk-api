---
UID: NF:wmsdkidl.IWMWriterPreprocess.GetMaxPreprocessingPasses
title: IWMWriterPreprocess::GetMaxPreprocessingPasses (wmsdkidl.h)
description: The GetMaxPreprocessingPasses method retrieves the maximum number of preprocessing passes for a specified input stream.
helpviewer_keywords: ["GetMaxPreprocessingPasses","GetMaxPreprocessingPasses method [windows Media Format]","GetMaxPreprocessingPasses method [windows Media Format]","IWMWriterPreprocess interface","IWMWriterPreprocess interface [windows Media Format]","GetMaxPreprocessingPasses method","IWMWriterPreprocess.GetMaxPreprocessingPasses","IWMWriterPreprocess::GetMaxPreprocessingPasses","IWMWriterPreprocessGetMaxPreprocessingPasses","wmformat.iwmwriterpreprocess_getmaxpreprocessingpasses","wmsdkidl/IWMWriterPreprocess::GetMaxPreprocessingPasses"]
old-location: wmformat\iwmwriterpreprocess_getmaxpreprocessingpasses.htm
tech.root: wmformat
ms.assetid: 6acdc536-8b38-4fd4-9705-f4399dfc3faa
ms.date: 12/05/2018
ms.keywords: GetMaxPreprocessingPasses, GetMaxPreprocessingPasses method [windows Media Format], GetMaxPreprocessingPasses method [windows Media Format],IWMWriterPreprocess interface, IWMWriterPreprocess interface [windows Media Format],GetMaxPreprocessingPasses method, IWMWriterPreprocess.GetMaxPreprocessingPasses, IWMWriterPreprocess::GetMaxPreprocessingPasses, IWMWriterPreprocessGetMaxPreprocessingPasses, wmformat.iwmwriterpreprocess_getmaxpreprocessingpasses, wmsdkidl/IWMWriterPreprocess::GetMaxPreprocessingPasses
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
 - IWMWriterPreprocess::GetMaxPreprocessingPasses
 - wmsdkidl/IWMWriterPreprocess::GetMaxPreprocessingPasses
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
 - IWMWriterPreprocess.GetMaxPreprocessingPasses
---

# IWMWriterPreprocess::GetMaxPreprocessingPasses


## -description

The <b>GetMaxPreprocessingPasses</b> method retrieves the maximum number of preprocessing passes for a specified input stream.

## -parameters

### -param dwInputNum [in]

<b>DWORD</b> containing the input number for which you want to get the maximum number of preprocessing passes.

### -param dwFlags [in]

Reserved. Set to zero.

### -param pdwMaxNumPasses [out]

Pointer to a <b>DWORD</b> that will receive the maximum number of preprocessing passes. If the codec supports two-pass encoding, this value is 1, as the final pass is not counted.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwMaxNumPasses</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwInputNum</i> specifies an invalid input stream number.

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

</td>
</tr>
</table>

## -remarks

If no preprocessing is supported for the specified input, <i>pdwMaxNumPasses</i> contains zero upon return.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess">IWMWriterPreprocess Interface</a>