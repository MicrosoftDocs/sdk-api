---
UID: NF:wmsdkidl.IWMReaderAdvanced4.CanSaveFileAs
title: IWMReaderAdvanced4::CanSaveFileAs (wmsdkidl.h)
description: The CanSaveFileAs method ascertains whether the content being played by the reader can be saved using the IWMReaderAdvanced2::SaveFileAs method.
helpviewer_keywords: ["CanSaveFileAs","CanSaveFileAs method [windows Media Format]","CanSaveFileAs method [windows Media Format]","IWMReaderAdvanced4 interface","IWMReaderAdvanced4 interface [windows Media Format]","CanSaveFileAs method","IWMReaderAdvanced4.CanSaveFileAs","IWMReaderAdvanced4::CanSaveFileAs","IWMReaderAdvanced4CanSaveFileAs","wmformat.iwmreaderadvanced4_cansavefileas","wmsdkidl/IWMReaderAdvanced4::CanSaveFileAs"]
old-location: wmformat\iwmreaderadvanced4_cansavefileas.htm
tech.root: wmformat
ms.assetid: ed4f31b6-e20f-432c-a1ec-954d85ce3a3d
ms.date: 12/05/2018
ms.keywords: CanSaveFileAs, CanSaveFileAs method [windows Media Format], CanSaveFileAs method [windows Media Format],IWMReaderAdvanced4 interface, IWMReaderAdvanced4 interface [windows Media Format],CanSaveFileAs method, IWMReaderAdvanced4.CanSaveFileAs, IWMReaderAdvanced4::CanSaveFileAs, IWMReaderAdvanced4CanSaveFileAs, wmformat.iwmreaderadvanced4_cansavefileas, wmsdkidl/IWMReaderAdvanced4::CanSaveFileAs
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
 - IWMReaderAdvanced4::CanSaveFileAs
 - wmsdkidl/IWMReaderAdvanced4::CanSaveFileAs
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
 - IWMReaderAdvanced4.CanSaveFileAs
---

# IWMReaderAdvanced4::CanSaveFileAs


## -description

The <b>CanSaveFileAs</b> method ascertains whether the content being played by the reader can be saved using the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas">IWMReaderAdvanced2::SaveFileAs</a> method.

## -parameters

### -param pfCanSave [out]

Pointer to a Boolean value that is set to True if that the content being read can be saved.

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
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>