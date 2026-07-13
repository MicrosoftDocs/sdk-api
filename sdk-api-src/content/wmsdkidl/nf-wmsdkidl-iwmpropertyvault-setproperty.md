---
UID: NF:wmsdkidl.IWMPropertyVault.SetProperty
title: IWMPropertyVault::SetProperty (wmsdkidl.h)
description: The SetProperty method sets the values for a property. If the property named already exists in the property vault, SetProperty changes its value as specified. If the property named does not exist, SetProperty adds it to the property vault.
helpviewer_keywords: ["IWMPropertyVault interface [windows Media Format]","SetProperty method","IWMPropertyVault.SetProperty","IWMPropertyVault::SetProperty","IWMPropertyVaultSetProperty","SetProperty","SetProperty method [windows Media Format]","SetProperty method [windows Media Format]","IWMPropertyVault interface","wmformat.iwmpropertyvault_setproperty","wmsdkidl/IWMPropertyVault::SetProperty"]
old-location: wmformat\iwmpropertyvault_setproperty.htm
tech.root: wmformat
ms.assetid: 0fae0ecf-efa9-46d0-8324-4065f351291e
ms.date: 4/26/2023
ms.keywords: IWMPropertyVault interface [windows Media Format],SetProperty method, IWMPropertyVault.SetProperty, IWMPropertyVault::SetProperty, IWMPropertyVaultSetProperty, SetProperty, SetProperty method [windows Media Format], SetProperty method [windows Media Format],IWMPropertyVault interface, wmformat.iwmpropertyvault_setproperty, wmsdkidl/IWMPropertyVault::SetProperty
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
 - IWMPropertyVault::SetProperty
 - wmsdkidl/IWMPropertyVault::SetProperty
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
 - IWMPropertyVault.SetProperty
---

# IWMPropertyVault::SetProperty


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetProperty</b> method sets the values for a property. If the property named already exists in the property vault, <b>SetProperty</b> changes its value as specified. If the property named does not exist, <b>SetProperty</b> adds it to the property vault.

## -parameters

### -param pszName [in]

Pointer to a <b>null</b>-terminated string containing the name of the property to set.

The following table lists the property names supported by the <b>IWMPropertyVault</b> interface. The property used dictates the data type and meaning of the data pointed to by <i>pValue</i>; these values are also in the table. All of these values apply to stream configuration objects.

<table>
<tr>
<th>Global constant
                </th>
<th>Data type
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>g_wszOriginalSourceFormatTag</td>
<td><b>WMT_TYPE_WORD
                </b></td>
<td>When transcoding with smart recompression, set to the <b>WAVEFORMATEX.wFormatTag</b> used in the original encoding.This value is now obsolete, use g_wszOriginalWaveFormat instead.

</td>
</tr>
<tr>
<td>g_wszOriginalWaveFormat</td>
<td><b>WMT_TYPE_BINARY
                </b></td>
<td>When transcoding with smart recompression, set to the <a href="/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)">WAVEFORMATEX</a> structure used in the original encoding.</td>
</tr>
<tr>
<td>g_wszEDL</td>
<td><b>WMT_TYPE_STRING
                </b></td>
<td>For Windows Media Audio 9 Voice streams, use to manually specify sections of the stream that contain music. This property should only be used if the automatic selection by the codec is creating a poor quality stream.</td>
</tr>
<tr>
<td>g_wszComplexity</td>
<td><b>WMT_TYPE_WORD
                </b></td>
<td>Set to the complexity setting desired. You can find the complexity levels supported by a codec by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop">IWMCodecInfo3::GetCodecProp</a>.</td>
</tr>
<tr>
<td>g_wszDecoderComplexityRequested</td>
<td><b>WMT_TYPE_STRING
                </b></td>
<td>Set to the string value of the device conformance template that you would like the stream to be encoded to. For audio there is only one string value, for video, us the two-letter designation before the ampersand. For more information, see <a href="/windows/desktop/wmformat/device-conformance-template-parameters">Device Conformance Template Parameters</a>.</td>
</tr>
<tr>
<td>g_wszPeakValue</td>
<td><b>WMT_TYPE_DWORD
                </b></td>
<td>Set to the peak volume level by the audio codec. Used for normalization. Do not manually set.</td>
</tr>
<tr>
<td>g_wszAverageLevel</td>
<td><b>WMT_TYPE_DWORD
                </b></td>
<td>Set to the average volume level by the audio codec. Used for normalization. Do not manually set.</td>
</tr>
<tr>
<td>g_wszFold6To2Channels3</td>
<td><b>WMT_TYPE_STRING
                </b></td>
<td>Set to the value for 6 to 2 channel fold down. Use for multichannel audio.</td>
</tr>
<tr>
<td>g_wszFoldToChannelsTemplate</td>
<td><b>WMT_TYPE_STRING
                </b></td>
<td>Template string to create other fold down values.</td>
</tr>
<tr>
<td>g_wszMusicSpeechClassMode</td>
<td><b>WMT_TYPE_STRING
                </b></td>
<td>Set to the type of encoding you want to use with the Windows Media Audio 9 Voice codec. Can be set to:g_wszMusicClassMode

g_wszSpeechClassMode

g_wszMixedClassMode

</td>
</tr>
</table>
 

In addition to the values in the table, the settings for variable bit rate encoding are set using this method. For more information, see <a href="/windows/desktop/wmformat/configuring-vbr-streams">Configuring VBR Streams</a>.

### -param pType [in]

Pointer to a member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type. This parameter specifies the type of data pointed to by <i>pValue</i>.

### -param pValue [in]

Pointer to a data buffer containing the value of the property. This value can be one of several types. The type of data that the buffer contains on output is specified by the value of <i>pType</i>.

### -param dwSize [in]

<b>DWORD</b> containing the size, in bytes, of the data at <i>pValue</i>.

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
<i>pszName</i> is <b>NULL</b> or points to a zero length string.

OR

The type specified at <i>pValue</i> does not agree with the size in bytes specified by <i>dwSize</i>.

OR

You are trying to delete a property that does not exist in the property vault.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method cannot allocate memory for a new property.

OR

The method cannot allocate memory for a new value.

</td>
</tr>
</table>

## -remarks

Properties set on stream configuration objects using this method are persisted in the profile to which the stream configuration is added. However, files created using that profile do not contain these properties in the header information.

<b>SetProperty</b> does not return the index of the property affected. New properties are assigned indexes sequentially.

You can remove a property using <b>SetProperty</b> by passing either <b>NULL</b> as <i>pValue</i> or 0 as <i>dwSize</i>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault">IWMPropertyVault Interface</a>