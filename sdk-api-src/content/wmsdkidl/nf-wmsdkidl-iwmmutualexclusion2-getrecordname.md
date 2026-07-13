---
UID: NF:wmsdkidl.IWMMutualExclusion2.GetRecordName
title: IWMMutualExclusion2::GetRecordName (wmsdkidl.h)
description: The GetRecordName method retrieves the name of the specified record. A record has a name only if a name has been assigned using the IWMMutualExclusion2::SetRecordName method.
helpviewer_keywords: ["GetRecordName","GetRecordName method [windows Media Format]","GetRecordName method [windows Media Format]","IWMMutualExclusion2 interface","IWMMutualExclusion2 interface [windows Media Format]","GetRecordName method","IWMMutualExclusion2.GetRecordName","IWMMutualExclusion2::GetRecordName","IWMMutualExclusion2GetRecordName","wmformat.iwmmutualexclusion2_getrecordname","wmsdkidl/IWMMutualExclusion2::GetRecordName"]
old-location: wmformat\iwmmutualexclusion2_getrecordname.htm
tech.root: wmformat
ms.assetid: 7508a473-77ae-49ce-b041-2d171193e730
ms.date: 4/26/2023
ms.keywords: GetRecordName, GetRecordName method [windows Media Format], GetRecordName method [windows Media Format],IWMMutualExclusion2 interface, IWMMutualExclusion2 interface [windows Media Format],GetRecordName method, IWMMutualExclusion2.GetRecordName, IWMMutualExclusion2::GetRecordName, IWMMutualExclusion2GetRecordName, wmformat.iwmmutualexclusion2_getrecordname, wmsdkidl/IWMMutualExclusion2::GetRecordName
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
 - IWMMutualExclusion2::GetRecordName
 - wmsdkidl/IWMMutualExclusion2::GetRecordName
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
 - IWMMutualExclusion2.GetRecordName
---

# IWMMutualExclusion2::GetRecordName


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetRecordName</b> method retrieves the name of the specified record. A record has a name only if a name has been assigned using the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-setrecordname">IWMMutualExclusion2::SetRecordName</a> method.

## -parameters

### -param wRecordNumber [in]

<b>WORD</b> containing the number of the record for which you want to get the name.

### -param pwszRecordName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the record name. Pass <b>NULL</b> to retrieve the length of the name.

### -param pcchRecordName [in, out]

On input, a pointer to a variable containing the length of the <i>pwszRecordName</i> array in wide characters (2 bytes). On output, if the method succeeds, the variable contains the length of the name, including the terminating <b>null</b> character. However, if you pass <b>NULL</b> as <i>pwszRecordName</i>, this will be set to the required length on output.

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
<i>wRecordNumber</i> does not contain a valid record number.

OR

<i>pcchRecordName</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to access the record for an unspecified reason.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetRecordName</b> for each record name you want to retrieve. On the first call, pass <b>NULL</b> as <i>pwszRecordName</i>. On return, the value pointed to by <i>pcchRecordName</i> will be set to the number of wide characters, including the terminating <b>null</b> character, required to hold the record name. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszRecordName</i> on the second call.

Records are assigned numbers sequentially in the order they are created.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2">IWMMutualExclusion2 Interface</a>