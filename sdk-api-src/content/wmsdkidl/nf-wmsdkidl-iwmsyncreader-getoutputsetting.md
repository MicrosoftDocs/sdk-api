---
UID: NF:wmsdkidl.IWMSyncReader.GetOutputSetting
title: IWMSyncReader::GetOutputSetting (wmsdkidl.h)
description: The GetOutputSetting method retrieves a setting for a particular output by name.
helpviewer_keywords: ["GetOutputSetting","GetOutputSetting method [windows Media Format]","GetOutputSetting method [windows Media Format]","IWMSyncReader interface","IWMSyncReader interface [windows Media Format]","GetOutputSetting method","IWMSyncReader.GetOutputSetting","IWMSyncReader::GetOutputSetting","IWMSyncReaderGetOutputSetting","wmformat.iwmsyncreader_getoutputsetting","wmsdkidl/IWMSyncReader::GetOutputSetting"]
old-location: wmformat\iwmsyncreader_getoutputsetting.htm
tech.root: wmformat
ms.assetid: b96c84fd-a2e0-4fdb-a9c1-2e42b73f7a3e
ms.date: 4/26/2023
ms.keywords: GetOutputSetting, GetOutputSetting method [windows Media Format], GetOutputSetting method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetOutputSetting method, IWMSyncReader.GetOutputSetting, IWMSyncReader::GetOutputSetting, IWMSyncReaderGetOutputSetting, wmformat.iwmsyncreader_getoutputsetting, wmsdkidl/IWMSyncReader::GetOutputSetting
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
 - IWMSyncReader::GetOutputSetting
 - wmsdkidl/IWMSyncReader::GetOutputSetting
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
 - IWMSyncReader.GetOutputSetting
---

# IWMSyncReader::GetOutputSetting


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetOutputSetting</b> method retrieves a setting for a particular output by name.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.

### -param pszName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the name of the setting for which you want the value. For a list of global constants representing setting names, see <a href="/windows/desktop/wmformat/output-settings">Output Settings</a>.

### -param pType [out]

Pointer to a variable that receives one value from the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type. The value received specifies the type of data in <i>pValue</i>.

### -param pValue [out]

Pointer to a byte buffer containing the value. Pass <b>NULL</b> to retrieve the length of the buffer required.

### -param pcbLength [in, out]

On input, pointer to a variable containing the length of <i>pValue</i>. On output, the variable contains the number of bytes in <i>pValue</i> used.

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
<i>dwOutputNum</i> specifies an invalid output number.

OR

<i>pszName</i> or <i>pType</i> or <i>pcbLength</i> is <b>NULL</b>.

OR

<i>pszName</i> specifies an invalid setting name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
No file is open in the synchronous reader.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer size passed as <i>pcbLength</i> is not large enough to contain the setting value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>pszName</i> specifies an unsupported setting.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetOutputSetting</b> for each setting you want to retrieve. On the first call, pass <b>NULL</b> as <i>pValue</i>. On return, the value of <i>pcbLength</i> is set to the buffer size required to hold the value of the specified setting. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>pValue</i> on the second call.

If you pass a buffer as <i>pValue</i> that is not large enough to contain the data, an error code of ASF_E_BUFFERTOOSMALL is returned. When returning this error code, the method still sets the value of <i>pcbLength</i> to the correct size of the value.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting">IWMSyncReader::SetOutputSetting</a>