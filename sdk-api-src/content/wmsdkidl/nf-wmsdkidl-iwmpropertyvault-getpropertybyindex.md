---
UID: NF:wmsdkidl.IWMPropertyVault.GetPropertyByIndex
title: IWMPropertyVault::GetPropertyByIndex (wmsdkidl.h)
description: The GetPropertyByIndex method retrieves a property from the vault by its index value.
helpviewer_keywords: ["GetPropertyByIndex","GetPropertyByIndex method [windows Media Format]","GetPropertyByIndex method [windows Media Format]","IWMPropertyVault interface","IWMPropertyVault interface [windows Media Format]","GetPropertyByIndex method","IWMPropertyVault.GetPropertyByIndex","IWMPropertyVault::GetPropertyByIndex","IWMPropertyVaultGetPropertyByIndex","wmformat.iwmpropertyvault_getpropertybyindex","wmsdkidl/IWMPropertyVault::GetPropertyByIndex"]
old-location: wmformat\iwmpropertyvault_getpropertybyindex.htm
tech.root: wmformat
ms.assetid: edecc6d2-f784-4205-bd79-6098e553d5cd
ms.date: 4/26/2023
ms.keywords: GetPropertyByIndex, GetPropertyByIndex method [windows Media Format], GetPropertyByIndex method [windows Media Format],IWMPropertyVault interface, IWMPropertyVault interface [windows Media Format],GetPropertyByIndex method, IWMPropertyVault.GetPropertyByIndex, IWMPropertyVault::GetPropertyByIndex, IWMPropertyVaultGetPropertyByIndex, wmformat.iwmpropertyvault_getpropertybyindex, wmsdkidl/IWMPropertyVault::GetPropertyByIndex
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
 - IWMPropertyVault::GetPropertyByIndex
 - wmsdkidl/IWMPropertyVault::GetPropertyByIndex
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
 - IWMPropertyVault.GetPropertyByIndex
---

# IWMPropertyVault::GetPropertyByIndex


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetPropertyByIndex</b> method retrieves a property from the vault by its index value.

## -parameters

### -param dwIndex [in]

<b>DWORD</b> containing the property index.

### -param pszName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the name of the property.

### -param pdwNameLen [in, out]

On input, a pointer to a <b>DWORD</b> containing the length, in wide characters, of the string at <i>pszName</i>. On output, specifies the number of characters, including the terminating <b>null</b> character, required to hold the property name.

### -param pType [out]

Pointer to a member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type. This parameter specifies the type of data pointed to by <i>pValue</i>.

### -param pValue [out]

Pointer to a data buffer containing the value of the property. This value can be one of several types. The type of data that the buffer contains on output is specified by the value of <i>pType</i>.

### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> containing the size, in bytes, of the data at <i>pValue</i>.

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
<i>pdwNameLen</i> or <i>pdwSize</i> or <i>pType</i> is <b>NULL</b>.

OR

The index specified is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
One of the buffers (<i>pszName</i> or <i>pValue</i>) is not big enough to hold the property information.

</td>
</tr>
</table>

## -remarks

You must make two calls to <b>GetPropertyByIndex</b> to properly retrieve all of the information. On the first call, pass <b>NULL</b> for both <i>pszName</i> and <i>pValue</i>. When the call returns, <i>pdwNameLen</i> and <i>pdwSize</i> point to the correct sizes of their respective buffers. Then on the second call, pass properly sized buffers as <i>pszName</i> and <i>pValue</i> to receive the data.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault">IWMPropertyVault Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname">IWMPropertyVault::GetPropertyByName</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty">IWMPropertyVault::SetProperty</a>