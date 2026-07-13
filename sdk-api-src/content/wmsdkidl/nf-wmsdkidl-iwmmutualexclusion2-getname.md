---
UID: NF:wmsdkidl.IWMMutualExclusion2.GetName
title: IWMMutualExclusion2::GetName (wmsdkidl.h)
description: The GetName method retrieves the name of the current mutual exclusion object. A mutual exclusion object has a name only if a name has been assigned using the IWMMutualExclusion2::SetName method.
helpviewer_keywords: ["GetName","GetName method [windows Media Format]","GetName method [windows Media Format]","IWMMutualExclusion2 interface","IWMMutualExclusion2 interface [windows Media Format]","GetName method","IWMMutualExclusion2.GetName","IWMMutualExclusion2::GetName","IWMMutualExclusion2GetName","wmformat.iwmmutualexclusion2_getname","wmsdkidl/IWMMutualExclusion2::GetName"]
old-location: wmformat\iwmmutualexclusion2_getname.htm
tech.root: wmformat
ms.assetid: da62ed2e-7356-4b4e-b2c5-6c18ef806ba7
ms.date: 4/26/2023
ms.keywords: GetName, GetName method [windows Media Format], GetName method [windows Media Format],IWMMutualExclusion2 interface, IWMMutualExclusion2 interface [windows Media Format],GetName method, IWMMutualExclusion2.GetName, IWMMutualExclusion2::GetName, IWMMutualExclusion2GetName, wmformat.iwmmutualexclusion2_getname, wmsdkidl/IWMMutualExclusion2::GetName
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
 - IWMMutualExclusion2::GetName
 - wmsdkidl/IWMMutualExclusion2::GetName
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
 - IWMMutualExclusion2.GetName
---

# IWMMutualExclusion2::GetName


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetName</b> method retrieves the name of the current mutual exclusion object. A mutual exclusion object has a name only if a name has been assigned using the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-setname">IWMMutualExclusion2::SetName</a> method.

## -parameters

### -param pwszName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the name of the mutual exclusion object. Pass <b>NULL</b> to retrieve the length of the name.

### -param pcchName [in, out]

On input, a pointer to a variable containing the length of the <i>pwszName</i> array in wide characters (2 bytes). On output, if the method succeeds, the variable contains the length of the name, including the terminating <b>null</b> character.

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
The <i>pcchName</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

You can pass <i>pwszName</i> as <b>NULL</b> to retrieve the correct size of the name in <i>pcchName</i> and then make another call to this method with a properly sized string. If you do, the value you pass as <i>pcchName</i> is irrelevant. It will be replaced with the correct length of the name.

If you pass an address as <i>pwszName</i>, and the length you specified in <i>pcchName</i> is shorter than the number of characters required to store the name, <b>GetName</b> ignores <i>pwszName</i> and returns the correct number of characters in <i>pcchName</i>. In this case the method still returns S_OK.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2">IWMMutualExclusion2 Interface</a>