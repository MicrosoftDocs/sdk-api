---
UID: NF:wmsdkidl.IWMWriterAdvanced2.GetInputSetting
title: IWMWriterAdvanced2::GetInputSetting (wmsdkidl.h)
description: The GetInputSetting method retrieves a setting for a particular input by name.helpviewer_keywords: ["GetInputSetting","GetInputSetting method [windows Media Format]","GetInputSetting method [windows Media Format]","IWMWriterAdvanced2 interface","IWMWriterAdvanced2 interface [windows Media Format]","GetInputSetting method","IWMWriterAdvanced2.GetInputSetting","IWMWriterAdvanced2::GetInputSetting","IWMWriterAdvanced2GetInputSetting","wmformat.iwmwriteradvanced2_getinputsetting","wmsdkidl/IWMWriterAdvanced2::GetInputSetting"]
old-location: wmformat\iwmwriteradvanced2_getinputsetting.htm
tech.root: wmformat
ms.assetid: 3aea0bc6-94e7-41ab-aec3-7366f183bb01
ms.date: 12/05/2018
ms.keywords: GetInputSetting, GetInputSetting method [windows Media Format], GetInputSetting method [windows Media Format],IWMWriterAdvanced2 interface, IWMWriterAdvanced2 interface [windows Media Format],GetInputSetting method, IWMWriterAdvanced2.GetInputSetting, IWMWriterAdvanced2::GetInputSetting, IWMWriterAdvanced2GetInputSetting, wmformat.iwmwriteradvanced2_getinputsetting, wmsdkidl/IWMWriterAdvanced2::GetInputSetting
f1_keywords:
- wmsdkidl/IWMWriterAdvanced2.GetInputSetting
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
- IWMWriterAdvanced2.GetInputSetting
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterAdvanced2::GetInputSetting


## -description



The <b>GetInputSetting</b> method retrieves a setting for a particular input by name.




## -parameters




### -param dwInputNum [in]

<b>DWORD</b> containing the input number.


### -param pszName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the setting name. For a list of valid settings, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/input-settings">Input Settings</a>.


### -param pType [out]

Pointer to a value from the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type.


### -param pValue [out]

Pointer to a byte array containing the setting. The type of date is determined by <i>pType</i>. Pass <b>NULL</b> to retrieve the size of array required.


### -param pcbLength [in, out]

On input, pointer to the length of <i>pValue</i>. On output, pointer to a count of the bytes in <i>pValue</i> filled in by this method.


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

<i>pType</i>, <i>pcbLength</i>, or <i>pszName</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetInputSetting</b> for each setting you want to retrieve. On the first call, pass <b>NULL</b> as <i>pValue</i>. On return, the value pointed to by <i>pcbLength</i> is set to the buffer size required to hold the setting value. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>pValue</i> on the second call.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2">IWMWriterAdvanced2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting">IWMWriterAdvanced2::SetInputSetting</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/input-formats-input-settings-and-data-unit-extensions">Input Formats, Input Settings, and Data Unit Extensions</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/to-set-input-settings">To Set Input Settings</a>
 

 

