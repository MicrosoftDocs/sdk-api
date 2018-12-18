---
UID: NF:wmsdkidl.IWMWriterAdvanced2.GetInputSetting
title: IWMWriterAdvanced2::GetInputSetting
author: windows-sdk-content
description: The GetInputSetting method retrieves a setting for a particular input by name.
old-location: wmformat\iwmwriteradvanced2_getinputsetting.htm
tech.root: wmformat
ms.assetid: 3aea0bc6-94e7-41ab-aec3-7366f183bb01
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInputSetting, GetInputSetting method [windows Media Format], GetInputSetting method [windows Media Format],IWMWriterAdvanced2 interface, IWMWriterAdvanced2 interface [windows Media Format],GetInputSetting method, IWMWriterAdvanced2.GetInputSetting, IWMWriterAdvanced2::GetInputSetting, IWMWriterAdvanced2GetInputSetting, wmformat.iwmwriteradvanced2_getinputsetting, wmsdkidl/IWMWriterAdvanced2::GetInputSetting
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterAdvanced2::GetInputSetting


## -description



The <b>GetInputSetting</b> method retrieves a setting for a particular input by name.




## -parameters




### -param dwInputNum [in]

<b>DWORD</b> containing the input number.


### -param pszName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the setting name. For a list of valid settings, see <a href="https://msdn.microsoft.com/23adbb64-5733-4198-8f2b-d02052ddb848">Input Settings</a>.


### -param pType [out]

Pointer to a value from the <a href="https://msdn.microsoft.com/en-us/library/Dd757834(v=VS.85).aspx">WMT_ATTR_DATATYPE</a> enumeration type.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd798721(v=VS.85).aspx">IWMWriterAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798723(v=VS.85).aspx">IWMWriterAdvanced2::SetInputSetting</a>



<a href="https://msdn.microsoft.com/8e8a0ec8-cb7c-4483-86b0-142ea9f2b835">Input Formats, Input Settings, and Data Unit Extensions</a>



<a href="https://msdn.microsoft.com/288801a7-793f-43bd-9c5a-f9e1bd86ecc3">To Set Input Settings</a>
 

 

