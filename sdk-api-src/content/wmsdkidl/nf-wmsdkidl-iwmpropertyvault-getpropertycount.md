---
UID: NF:wmsdkidl.IWMPropertyVault.GetPropertyCount
title: IWMPropertyVault::GetPropertyCount (wmsdkidl.h)
description: The GetPropertyCount method retrieves a count of all the properties in the property vault.
helpviewer_keywords: ["GetPropertyCount","GetPropertyCount method [windows Media Format]","GetPropertyCount method [windows Media Format]","IWMPropertyVault interface","IWMPropertyVault interface [windows Media Format]","GetPropertyCount method","IWMPropertyVault.GetPropertyCount","IWMPropertyVault::GetPropertyCount","IWMPropertyVaultGetPropertyCount","wmformat.iwmpropertyvault_getpropertycount","wmsdkidl/IWMPropertyVault::GetPropertyCount"]
old-location: wmformat\iwmpropertyvault_getpropertycount.htm
tech.root: wmformat
ms.assetid: 2045183d-8683-416f-bda0-87c5fecf8c11
ms.date: 4/26/2023
ms.keywords: GetPropertyCount, GetPropertyCount method [windows Media Format], GetPropertyCount method [windows Media Format],IWMPropertyVault interface, IWMPropertyVault interface [windows Media Format],GetPropertyCount method, IWMPropertyVault.GetPropertyCount, IWMPropertyVault::GetPropertyCount, IWMPropertyVaultGetPropertyCount, wmformat.iwmpropertyvault_getpropertycount, wmsdkidl/IWMPropertyVault::GetPropertyCount
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
 - IWMPropertyVault::GetPropertyCount
 - wmsdkidl/IWMPropertyVault::GetPropertyCount
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
 - IWMPropertyVault.GetPropertyCount
---

# IWMPropertyVault::GetPropertyCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetPropertyCount</b> method retrieves a count of all the properties in the property vault.

## -parameters

### -param pdwCount [out]

Pointer to a <b>DWORD</b> that will receive the property count.

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
pdwCount is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault">IWMPropertyVault Interface</a>