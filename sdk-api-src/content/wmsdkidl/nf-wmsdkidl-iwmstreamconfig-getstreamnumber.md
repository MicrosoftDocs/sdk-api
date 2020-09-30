---
UID: NF:wmsdkidl.IWMStreamConfig.GetStreamNumber
title: IWMStreamConfig::GetStreamNumber (wmsdkidl.h)
description: The GetStreamNumber method retrieves the stream number.
helpviewer_keywords: ["GetStreamNumber","GetStreamNumber method [windows Media Format]","GetStreamNumber method [windows Media Format]","IWMStreamConfig interface","IWMStreamConfig interface [windows Media Format]","GetStreamNumber method","IWMStreamConfig.GetStreamNumber","IWMStreamConfig::GetStreamNumber","IWMStreamConfigGetStreamNumber","wmformat.iwmstreamconfig_getstreamnumber","wmsdkidl/IWMStreamConfig::GetStreamNumber"]
old-location: wmformat\iwmstreamconfig_getstreamnumber.htm
tech.root: wmformat
ms.assetid: 2996c897-eb38-4432-8bf7-549023ab00f5
ms.date: 12/05/2018
ms.keywords: GetStreamNumber, GetStreamNumber method [windows Media Format], GetStreamNumber method [windows Media Format],IWMStreamConfig interface, IWMStreamConfig interface [windows Media Format],GetStreamNumber method, IWMStreamConfig.GetStreamNumber, IWMStreamConfig::GetStreamNumber, IWMStreamConfigGetStreamNumber, wmformat.iwmstreamconfig_getstreamnumber, wmsdkidl/IWMStreamConfig::GetStreamNumber
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
 - IWMStreamConfig::GetStreamNumber
 - wmsdkidl/IWMStreamConfig::GetStreamNumber
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
 - IWMStreamConfig.GetStreamNumber
---

# IWMStreamConfig::GetStreamNumber


## -description

The <b>GetStreamNumber</b> method retrieves the stream number.

## -parameters

### -param pwStreamNum [out]

Pointer to a <b>WORD</b> containing the stream number. Stream numbers must be in the range of 1 through 63.

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
The <i>pwStreamNum</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber">IWMStreamConfig::SetStreamNumber</a>