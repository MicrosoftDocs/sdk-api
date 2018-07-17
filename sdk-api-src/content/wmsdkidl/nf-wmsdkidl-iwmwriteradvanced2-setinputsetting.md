---
UID: NF:wmsdkidl.IWMWriterAdvanced2.SetInputSetting
title: IWMWriterAdvanced2::SetInputSetting
author: windows-sdk-content
description: The SetInputSetting method specifies a named setting for a particular input.
old-location: wmformat\iwmwriteradvanced2_setinputsetting.htm
old-project: wmformat
ms.assetid: a920bfe8-1f95-4957-b6c4-9749d5e10ee3
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWMWriterAdvanced2 interface [windows Media Format],SetInputSetting method, IWMWriterAdvanced2.SetInputSetting, IWMWriterAdvanced2::SetInputSetting, IWMWriterAdvanced2SetInputSetting, SetInputSetting, SetInputSetting method [windows Media Format], SetInputSetting method [windows Media Format],IWMWriterAdvanced2 interface, wmformat.iwmwriteradvanced2_setinputsetting, wmsdkidl/IWMWriterAdvanced2::SetInputSetting
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterAdvanced2::SetInputSetting


## -description



The <b>SetInputSetting</b> method specifies a named setting for a particular input.




## -parameters




### -param dwInputNum [in]

<b>DWORD</b> containing the input number.


### -param pszName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the setting name. For a list of valid settings, see <a href="https://msdn.microsoft.com/23adbb64-5733-4198-8f2b-d02052ddb848">Input Settings</a>.


### -param Type [in]

Pointer to a value from the <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> enumeration type.


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

Only g_wszDeinterlaceMode, g_wszInitialPatternForInverseTelecine, g_wszInterlacedCoding, and g_wszJPEGCompressionQuality can be set after <a href="https://msdn.microsoft.com/df511ff0-a87b-442a-85bd-c8d924ab2047">IWMWriter::BeginWriting</a> has been called.




## -see-also




<a href="https://msdn.microsoft.com/94790b67-690c-4a0f-9b82-801bfcec9eb0">IWMWriterAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/3aea0bc6-94e7-41ab-aec3-7366f183bb01">IWMWriterAdvanced2::GetInputSetting</a>



<a href="https://msdn.microsoft.com/8e8a0ec8-cb7c-4483-86b0-142ea9f2b835">Input Formats, Input Settings, and Data Unit Extensions</a>



<a href="https://msdn.microsoft.com/288801a7-793f-43bd-9c5a-f9e1bd86ecc3">To Set Input Settings</a>
 

 

