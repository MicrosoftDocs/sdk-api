---
UID: NF:wmsdkidl.IWMReaderAdvanced2.GetOutputSetting
title: IWMReaderAdvanced2::GetOutputSetting (wmsdkidl.h)
description: The GetOutputSetting method retrieves a setting for a particular output by name.
helpviewer_keywords: ["GetOutputSetting","GetOutputSetting method [windows Media Format]","GetOutputSetting method [windows Media Format]","IWMReaderAdvanced2 interface","IWMReaderAdvanced2 interface [windows Media Format]","GetOutputSetting method","IWMReaderAdvanced2.GetOutputSetting","IWMReaderAdvanced2::GetOutputSetting","IWMReaderAdvanced2GetOutputSetting","wmformat.iwmreaderadvanced2_getoutputsetting","wmsdkidl/IWMReaderAdvanced2::GetOutputSetting"]
old-location: wmformat\iwmreaderadvanced2_getoutputsetting.htm
tech.root: wmformat
ms.assetid: a46da973-8f2f-48b8-9a74-d54e67f68a83
ms.date: 4/26/2023
ms.keywords: GetOutputSetting, GetOutputSetting method [windows Media Format], GetOutputSetting method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced2 interface [windows Media Format],GetOutputSetting method, IWMReaderAdvanced2.GetOutputSetting, IWMReaderAdvanced2::GetOutputSetting, IWMReaderAdvanced2GetOutputSetting, wmformat.iwmreaderadvanced2_getoutputsetting, wmsdkidl/IWMReaderAdvanced2::GetOutputSetting
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
 - IWMReaderAdvanced2::GetOutputSetting
 - wmsdkidl/IWMReaderAdvanced2::GetOutputSetting
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
 - IWMReaderAdvanced2.GetOutputSetting
---

# IWMReaderAdvanced2::GetOutputSetting


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetOutputSetting</b> method retrieves a setting for a particular output by name.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.

### -param pszName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the setting name. For a list of global constants representing setting names, see <a href="/windows/desktop/wmformat/output-settings">Output Settings</a>.

### -param pType [out]

Pointer to a member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type that specifies the type of the value.

### -param pValue [out]

Pointer to a byte buffer containing the value. Pass <b>NULL</b> to retrieve the length of the buffer required.

### -param pcbLength [in, out]

On input, pointer to a variable containing the length of <i>pValue</i>. On output, the variable contains the number of bytes in <i>pValue</i>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

You should make two calls to <b>GetOutputSetting</b>. On the first call, pass <b>NULL</b> for <i>pValue</i>. On return, the value pointed to by <i>pcbLength</i> is set to the buffer size required to hold the setting value. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>pValue</i> on the second call.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>