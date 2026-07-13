---
UID: NF:mfobjects.IMFPluginControl.GetPreferredClsidByIndex
title: IMFPluginControl::GetPreferredClsidByIndex (mfobjects.h)
description: The IMFPluginControl::GetPreferredClsidByIndex (mfobjects.h) method gets a class identifier (CLSID) from the preferred list, specified by index value.
helpviewer_keywords: ["GetPreferredClsidByIndex","GetPreferredClsidByIndex method [Media Foundation]","GetPreferredClsidByIndex method [Media Foundation]","IMFPluginControl interface","IMFPluginControl interface [Media Foundation]","GetPreferredClsidByIndex method","IMFPluginControl.GetPreferredClsidByIndex","IMFPluginControl::GetPreferredClsidByIndex","mf.imfplugincontrol_imfplugincontrol__getpreferredclsidbyindex","mfobjects/IMFPluginControl::GetPreferredClsidByIndex"]
old-location: mf\imfplugincontrol_imfplugincontrol__getpreferredclsidbyindex.htm
tech.root: medfound
ms.assetid: d99511ec-ac22-4166-b944-b0136ffcf01a
ms.date: 08/05/2022
ms.keywords: GetPreferredClsidByIndex, GetPreferredClsidByIndex method [Media Foundation], GetPreferredClsidByIndex method [Media Foundation],IMFPluginControl interface, IMFPluginControl interface [Media Foundation],GetPreferredClsidByIndex method, IMFPluginControl.GetPreferredClsidByIndex, IMFPluginControl::GetPreferredClsidByIndex, mf.imfplugincontrol_imfplugincontrol__getpreferredclsidbyindex, mfobjects/IMFPluginControl::GetPreferredClsidByIndex
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPluginControl::GetPreferredClsidByIndex
 - mfobjects/IMFPluginControl::GetPreferredClsidByIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMFPluginControl.GetPreferredClsidByIndex
---

# IMFPluginControl::GetPreferredClsidByIndex


## -description

Gets a class identifier (CLSID) from the preferred list, specified by index value.

## -parameters

### -param pluginType [in]

Member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_type">MF_Plugin_Type</a> enumeration, specifying the type of object to enumerate.

### -param index [in]

The zero-based index of the CLSID to retrieve.

### -param selector [out]

Receives the key name associated with the CLSID. The caller must free the memory for the returned string by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function. For more information about the format of key names, see the Remarks section of <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a>.

### -param clsid [out]

Receives the CLSID at the specified index.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>
</td>
<td width="60%">
The <i>index</i> parameter is out of range.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a>