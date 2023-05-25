---
UID: NF:wmsdkidl.IWMInputMediaProps.GetGroupName
title: IWMInputMediaProps::GetGroupName (wmsdkidl.h)
description: The GetGroupName method is not implemented, and returns an empty string.
helpviewer_keywords: ["GetGroupName","GetGroupName method [windows Media Format]","GetGroupName method [windows Media Format]","IWMInputMediaProps interface","IWMInputMediaProps interface [windows Media Format]","GetGroupName method","IWMInputMediaProps.GetGroupName","IWMInputMediaProps::GetGroupName","IWMInputMediaPropsGetGroupName","wmformat.iwminputmediaprops_getgroupname","wmsdkidl/IWMInputMediaProps::GetGroupName"]
old-location: wmformat\iwminputmediaprops_getgroupname.htm
tech.root: wmformat
ms.assetid: 795cd065-62f1-4346-b2ff-f77ec4306d64
ms.date: 4/26/2023
ms.keywords: GetGroupName, GetGroupName method [windows Media Format], GetGroupName method [windows Media Format],IWMInputMediaProps interface, IWMInputMediaProps interface [windows Media Format],GetGroupName method, IWMInputMediaProps.GetGroupName, IWMInputMediaProps::GetGroupName, IWMInputMediaPropsGetGroupName, wmformat.iwminputmediaprops_getgroupname, wmsdkidl/IWMInputMediaProps::GetGroupName
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
 - IWMInputMediaProps::GetGroupName
 - wmsdkidl/IWMInputMediaProps::GetGroupName
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
 - IWMInputMediaProps.GetGroupName
---

# IWMInputMediaProps::GetGroupName


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetGroupName</b> method is not implemented, and returns an empty string.

## -parameters

### -param pwszName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the name. Pass <b>NULL</b> to retrieve the length required for the name.

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
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszName</i> parameter is not large enough.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops">IWMInputMediaProps Interface</a>