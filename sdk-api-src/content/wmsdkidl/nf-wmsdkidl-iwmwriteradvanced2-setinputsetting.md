---
UID: NF:wmsdkidl.IWMWriterAdvanced2.SetInputSetting
title: IWMWriterAdvanced2::SetInputSetting (wmsdkidl.h)
description: The SetInputSetting method specifies a named setting for a particular input.
helpviewer_keywords: ["IWMWriterAdvanced2 interface [windows Media Format]","SetInputSetting method","IWMWriterAdvanced2.SetInputSetting","IWMWriterAdvanced2::SetInputSetting","IWMWriterAdvanced2SetInputSetting","SetInputSetting","SetInputSetting method [windows Media Format]","SetInputSetting method [windows Media Format]","IWMWriterAdvanced2 interface","wmformat.iwmwriteradvanced2_setinputsetting","wmsdkidl/IWMWriterAdvanced2::SetInputSetting"]
old-location: wmformat\iwmwriteradvanced2_setinputsetting.htm
tech.root: wmformat
ms.assetid: a920bfe8-1f95-4957-b6c4-9749d5e10ee3
ms.date: 4/26/2023
ms.keywords: IWMWriterAdvanced2 interface [windows Media Format],SetInputSetting method, IWMWriterAdvanced2.SetInputSetting, IWMWriterAdvanced2::SetInputSetting, IWMWriterAdvanced2SetInputSetting, SetInputSetting, SetInputSetting method [windows Media Format], SetInputSetting method [windows Media Format],IWMWriterAdvanced2 interface, wmformat.iwmwriteradvanced2_setinputsetting, wmsdkidl/IWMWriterAdvanced2::SetInputSetting
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
 - IWMWriterAdvanced2::SetInputSetting
 - wmsdkidl/IWMWriterAdvanced2::SetInputSetting
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
 - IWMWriterAdvanced2.SetInputSetting
---

# IWMWriterAdvanced2::SetInputSetting


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetInputSetting</b> method specifies a named setting for a particular input.

## -parameters

### -param dwInputNum [in]

<b>DWORD</b> containing the input number.

### -param pszName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the setting name. For a list of valid settings, see <a href="/windows/desktop/wmformat/input-settings">Input Settings</a>.

### -param Type [in]

Pointer to a value from the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type.

### -param pValue [in]

Pointer to a byte array containing the setting.

### -param cbLength [in]

Size of <i>pValue</i>, in bytes.

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
<dt><b>NS_E_NOT_CONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
The input profile has not yet been set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwInputNum</i> is larger than the number of existing inputs

OR

<i>pValue</i> or <i>pszName</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
This setting cannot be changed while the writer is running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
</table>

## -remarks

The encoding settings set with this method are not persisted in the output file. If you want your custom player to have access to this information, you must save the values as custom metadata attributes in the file header.

Only g_wszDeinterlaceMode, g_wszInitialPatternForInverseTelecine, g_wszInterlacedCoding, and g_wszJPEGCompressionQuality can be set after <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a> has been called.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2">IWMWriterAdvanced2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting">IWMWriterAdvanced2::GetInputSetting</a>



<a href="/windows/desktop/wmformat/input-formats-input-settings-and-data-unit-extensions">Input Formats, Input Settings, and Data Unit Extensions</a>



<a href="/windows/desktop/wmformat/to-set-input-settings">To Set Input Settings</a>