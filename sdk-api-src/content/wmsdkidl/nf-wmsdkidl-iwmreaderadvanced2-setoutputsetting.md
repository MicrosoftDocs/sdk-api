---
UID: NF:wmsdkidl.IWMReaderAdvanced2.SetOutputSetting
title: IWMReaderAdvanced2::SetOutputSetting (wmsdkidl.h)
description: The SetOutputSetting method specifies a named setting for a particular output.
helpviewer_keywords: ["IWMReaderAdvanced2 interface [windows Media Format]","SetOutputSetting method","IWMReaderAdvanced2.SetOutputSetting","IWMReaderAdvanced2::SetOutputSetting","IWMReaderAdvanced2SetOutputSetting","SetOutputSetting","SetOutputSetting method [windows Media Format]","SetOutputSetting method [windows Media Format]","IWMReaderAdvanced2 interface","wmformat.iwmreaderadvanced2_setoutputsetting","wmsdkidl/IWMReaderAdvanced2::SetOutputSetting"]
old-location: wmformat\iwmreaderadvanced2_setoutputsetting.htm
tech.root: wmformat
ms.assetid: 035a74d2-288d-4754-8cb2-4508b7fe4649
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced2 interface [windows Media Format],SetOutputSetting method, IWMReaderAdvanced2.SetOutputSetting, IWMReaderAdvanced2::SetOutputSetting, IWMReaderAdvanced2SetOutputSetting, SetOutputSetting, SetOutputSetting method [windows Media Format], SetOutputSetting method [windows Media Format],IWMReaderAdvanced2 interface, wmformat.iwmreaderadvanced2_setoutputsetting, wmsdkidl/IWMReaderAdvanced2::SetOutputSetting
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
 - IWMReaderAdvanced2::SetOutputSetting
 - wmsdkidl/IWMReaderAdvanced2::SetOutputSetting
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
 - IWMReaderAdvanced2.SetOutputSetting
---

# IWMReaderAdvanced2::SetOutputSetting


## -description

The <b>SetOutputSetting</b> method specifies a named setting for a particular output.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.

### -param pszName [in]

Pointer to a wide-character null-terminated string containing the name. For a list of global constants that represent setting names, see <a href="/windows/desktop/wmformat/output-settings">Output Settings</a>.

### -param Type [in]

Member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type that specifies the type of the value.

### -param pValue [in]

Pointer to a byte array containing the value.

### -param cbLength [in]

Size of <i>pValue</i>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getoutputsetting">IWMReaderAdvanced2::GetOutputSetting</a>