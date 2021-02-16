---
UID: NF:wmsdkidl.IWMMutualExclusion.SetType
title: IWMMutualExclusion::SetType (wmsdkidl.h)
description: The SetType method specifies the GUID of the type of mutual exclusion required.
helpviewer_keywords: ["IWMMutualExclusion interface [windows Media Format]","SetType method","IWMMutualExclusion.SetType","IWMMutualExclusion::SetType","IWMMutualExclusionSetType","SetType","SetType method [windows Media Format]","SetType method [windows Media Format]","IWMMutualExclusion interface","wmformat.iwmmutualexclusion_settype","wmsdkidl/IWMMutualExclusion::SetType"]
old-location: wmformat\iwmmutualexclusion_settype.htm
tech.root: wmformat
ms.assetid: 18796219-bc33-41b7-b2af-a23585c2500a
ms.date: 12/05/2018
ms.keywords: IWMMutualExclusion interface [windows Media Format],SetType method, IWMMutualExclusion.SetType, IWMMutualExclusion::SetType, IWMMutualExclusionSetType, SetType, SetType method [windows Media Format], SetType method [windows Media Format],IWMMutualExclusion interface, wmformat.iwmmutualexclusion_settype, wmsdkidl/IWMMutualExclusion::SetType
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
 - IWMMutualExclusion::SetType
 - wmsdkidl/IWMMutualExclusion::SetType
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
 - IWMMutualExclusion.SetType
---

# IWMMutualExclusion::SetType


## -description

The <b>SetType</b> method specifies the GUID of the type of mutual exclusion required.

## -parameters

### -param guidType [in]

GUID specifying the type of mutual exclusion. For a list of values, see <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype">IWMMutualExclusion::GetType</a>

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
Invalid type.

</td>
</tr>
</table>

## -remarks

If you create a multiple bit rate audio file, you may encounter problems streaming the file from Windows Media Services 4.1. To avoid problems, disable auto indexing by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setautoindexing">IWMWriterFileSink3::SetAutoIndexing</a> before writing the file.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion">IWMMutualExclusion Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype">IWMMutualExclusion::GetType</a>