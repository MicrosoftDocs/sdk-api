---
UID: NF:wmsdkidl.IWMOutputMediaProps.GetStreamGroupName
title: IWMOutputMediaProps::GetStreamGroupName (wmsdkidl.h)
description: The GetStreamGroupName method is not implemented in this release, and returns the empty string.
helpviewer_keywords: ["GetStreamGroupName","GetStreamGroupName method [windows Media Format]","GetStreamGroupName method [windows Media Format]","IWMOutputMediaProps interface","IWMOutputMediaProps interface [windows Media Format]","GetStreamGroupName method","IWMOutputMediaProps.GetStreamGroupName","IWMOutputMediaProps::GetStreamGroupName","IWMOutputMediaPropsGetStreamGroupName","wmformat.iwmoutputmediaprops_getstreamgroupname","wmsdkidl/IWMOutputMediaProps::GetStreamGroupName"]
old-location: wmformat\iwmoutputmediaprops_getstreamgroupname.htm
tech.root: wmformat
ms.assetid: 65251316-c98f-46a3-a0cf-164531ef0b46
ms.date: 4/26/2023
ms.keywords: GetStreamGroupName, GetStreamGroupName method [windows Media Format], GetStreamGroupName method [windows Media Format],IWMOutputMediaProps interface, IWMOutputMediaProps interface [windows Media Format],GetStreamGroupName method, IWMOutputMediaProps.GetStreamGroupName, IWMOutputMediaProps::GetStreamGroupName, IWMOutputMediaPropsGetStreamGroupName, wmformat.iwmoutputmediaprops_getstreamgroupname, wmsdkidl/IWMOutputMediaProps::GetStreamGroupName
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
 - IWMOutputMediaProps::GetStreamGroupName
 - wmsdkidl/IWMOutputMediaProps::GetStreamGroupName
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
 - IWMOutputMediaProps.GetStreamGroupName
---

# IWMOutputMediaProps::GetStreamGroupName


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetStreamGroupName</b> method is not implemented in this release, and returns the empty string.

## -parameters

### -param pwszName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the name. Pass <b>NULL</b> to retrieve the length of the name.

### -param pcchName [in, out]

On input, a pointer to a variable containing the length of the <i>pwszName</i> array in wide characters (2 bytes). On output, and if the method succeeds, the variable contains the length of the name, including the terminating <b>null</b> character.

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
The buffer pointed to by the <i>pwszName</i> parameter is not large enough.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetStreamGroupName</b>. On the first call, pass <b>NULL</b> as <i>pwszName</i>. On return, the value pointed to by <i>pcchName</i> is set to the number of wide characters, including the terminating <b>null</b> character, required to hold the stream group name. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszName</i> on the second call.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps Interface</a>