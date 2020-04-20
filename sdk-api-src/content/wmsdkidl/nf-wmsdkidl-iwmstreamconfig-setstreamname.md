---
UID: NF:wmsdkidl.IWMStreamConfig.SetStreamName
title: IWMStreamConfig::SetStreamName (wmsdkidl.h)
description: The SetStreamName method assigns a name to the stream represented by the stream configuration object.helpviewer_keywords: ["IWMStreamConfig interface [windows Media Format]","SetStreamName method","IWMStreamConfig.SetStreamName","IWMStreamConfig::SetStreamName","IWMStreamConfigSetStreamName","SetStreamName","SetStreamName method [windows Media Format]","SetStreamName method [windows Media Format]","IWMStreamConfig interface","wmformat.iwmstreamconfig_setstreamname","wmsdkidl/IWMStreamConfig::SetStreamName"]
old-location: wmformat\iwmstreamconfig_setstreamname.htm
tech.root: wmformat
ms.assetid: 90ab1591-eee7-4504-8d7f-475d90fa3b40
ms.date: 12/05/2018
ms.keywords: IWMStreamConfig interface [windows Media Format],SetStreamName method, IWMStreamConfig.SetStreamName, IWMStreamConfig::SetStreamName, IWMStreamConfigSetStreamName, SetStreamName, SetStreamName method [windows Media Format], SetStreamName method [windows Media Format],IWMStreamConfig interface, wmformat.iwmstreamconfig_setstreamname, wmsdkidl/IWMStreamConfig::SetStreamName
f1_keywords:
- wmsdkidl/IWMStreamConfig.SetStreamName
dev_langs:
- c++
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
- IWMStreamConfig.SetStreamName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMStreamConfig::SetStreamName


## -description



The <b>SetStreamName</b> method assigns a name to the stream represented by the stream configuration object.




## -parameters




### -param pwszStreamName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the stream name. Stream names are limited to 256 wide characters.


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
The <i>pwszStreamName</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method is purely for the convenience of the developer during profile manipulation and file writing. The name assigned using this method is not stored in the header section of ASF files created using the profile and is therefore not available through the reader object or synchronous reader object.

The new value will not take effect in the profile until you call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getstreamname">IWMStreamConfig::GetStreamName</a>
 

 

