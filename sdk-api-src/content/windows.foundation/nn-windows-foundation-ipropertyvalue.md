---
UID: NN:windows.foundation.IPropertyValue
title: IPropertyValue
author: windows-sdk-content
description: Represents a value in a Windows Runtime property store.
old-location: winrt\ipropertyvalue.htm
tech.root: WinRT
ms.assetid: 447625BA-F982-4155-9B05-E478E1229443
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPropertyValue, IPropertyValue interface [Windows Runtime], IPropertyValue interface [Windows Runtime],described, windows/IPropertyValue, winrt.ipropertyvalue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Foundation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.Foundation.h
api_name:
 - IPropertyValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValue interface


## -description


Represents a value in a Windows Runtime property store.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyValue</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>. <b>IPropertyValue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IPropertyValue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5877E4BD-5712-4426-A31F-079E16ED0B4A">GetBoolean</a>
</td>
<td align="left" width="63%">
Gets the 8-bit Boolean value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22ad7bab-87b1-41e8-ae65-1957e7c93b2e">GetBooleanArray</a>
</td>
<td align="left" width="63%">
Gets the array of 8-bit Boolean values that is stored in the current  <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46412359-A57E-489C-9992-5A30AB2DA8C4">GetChar16</a>
</td>
<td align="left" width="63%">
Gets the Unicode character that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0649a8b-8060-4e0f-956e-879fe4185b11">GetChar16Array</a>
</td>
<td align="left" width="63%">
Gets the the array of Unicode characters that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ffe8778-ce0e-46bb-9387-48c20d5dddfc">GetDateTime</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/b5533002-8a72-438d-a3d3-0902ffc21830">DateTime</a> value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76d18ef4-676c-4130-90e3-e74776e47f33">GetDateTimeArray</a>
</td>
<td align="left" width="63%">
Gets the array of <a href="https://msdn.microsoft.com/b5533002-8a72-438d-a3d3-0902ffc21830">DateTime</a> values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93EC7793-DAEF-4E1D-A9B8-2D79A3CBBBDC">GetDouble</a>
</td>
<td align="left" width="63%">
Gets the 64-bit floating point value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/197a3626-e349-4027-913c-e8203dad4fc1">GetDoubleArray</a>
</td>
<td align="left" width="63%">
Gets the array of 64-bit floating point values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d094f70f-dfd3-4601-b288-4f9f79479609">GetGuid</a>
</td>
<td align="left" width="63%">
Gets the GUID value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83d19a18-3cd4-4343-8609-12e9a65b8e37">GetGuidArray</a>
</td>
<td align="left" width="63%">
Gets the array of <a href="https://msdn.microsoft.com/library/system.guid.aspx">Guid</a> values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0af4f31f-e121-4cb2-8e83-c774bf25cae5">GetInspectableArray</a>
</td>
<td align="left" width="63%">
Gets the array of pointers to <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> objects that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1708DC2B-8247-4F58-ACF5-7003F914C9E1">GetInt32</a>
</td>
<td align="left" width="63%">
Gets the signed 32-bit integer value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ace88b14-951c-4482-a46d-12c4665c9450">GetInt32Array</a>
</td>
<td align="left" width="63%">
Gets the array of signed 32-bit integer values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FA3EB6F4-8D5A-4DBE-9A49-D21BC5A57EF3">GetInt64</a>
</td>
<td align="left" width="63%">
Gets the signed 64-bit integer value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bc05817-e9d4-427a-883d-495faf5d0ab0">GetInt64Array</a>
</td>
<td align="left" width="63%">
Gets the array of signed 64-bit integer values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c42dabae-008e-4dc2-b7dd-2856adc8e610">GetPoint</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/0cdd5b17-2f7e-4e17-896c-7d7784c8643d">Point</a> value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7df4ad4e-3ca6-4956-b907-02c2cb6e481b">GetPointArray</a>
</td>
<td align="left" width="63%">
Gets the array of <a href="https://msdn.microsoft.com/0cdd5b17-2f7e-4e17-896c-7d7784c8643d">Point</a> values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2333bd80-56db-4fa4-b696-269969fd1362">GetRect</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/420daab1-71e7-4610-b454-a49a64061f97">Rect</a> value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e1f39f6-0ccb-4841-ae5e-36adaf72a4ee">GetRectArray</a>
</td>
<td align="left" width="63%">
Gets the array of <a href="https://msdn.microsoft.com/420daab1-71e7-4610-b454-a49a64061f97">Rect</a> values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FA04F9A2-C222-451B-A6CE-8324BB51DA23">GetSingle</a>
</td>
<td align="left" width="63%">
Gets the 32-bit floating point value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4286901-92b2-4707-9da7-bb7abf83bb87">GetSingleArray</a>
</td>
<td align="left" width="63%">
Gets the array of 32-bit floating point values that is stored in the current <a href="https://msdn.microsoft.com/29a8e6e5-764b-4de9-84ea-97abdee6b02f">IPropertyValue</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c864cf0e-8e7e-44b0-93dc-3d2d9f2326a7">GetSize</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/8705adcb-a657-4b47-94ba-632bfb3779be">Size</a> value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f378c4d0-c3a2-4611-a471-0c77746602f6">GetSizeArray</a>
</td>
<td align="left" width="63%">
Gets the array of <a href="https://msdn.microsoft.com/8705adcb-a657-4b47-94ba-632bfb3779be">Size</a> values that is stored in the current <a href="https://msdn.microsoft.com/29a8e6e5-764b-4de9-84ea-97abdee6b02f">IPropertyValue</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56376A64-78F7-4C28-B3A7-9CE6594342E4">GetString</a>
</td>
<td align="left" width="63%">
Gets the string value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d256b888-efa0-470e-b54f-5cf8ddd6fd8a">GetStringArray</a>
</td>
<td align="left" width="63%">
Gets the array of string values that is stored in the current <a href="https://msdn.microsoft.com/29a8e6e5-764b-4de9-84ea-97abdee6b02f">IPropertyValue</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c78d584f-e2ef-4623-b45a-e26d2ec1518b">GetTimeSpan</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/fbc6ecc2-6372-4b15-9532-3cd68a72e7b4">TimeSpan</a> value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a52a665c-4c3a-4489-bd7b-e8ecb8dfe9cc">GetTimeSpanArray</a>
</td>
<td align="left" width="63%">
Gets the array of <a href="https://msdn.microsoft.com/fbc6ecc2-6372-4b15-9532-3cd68a72e7b4">TimeSpan</a> values that is stored in the current <a href="https://msdn.microsoft.com/29a8e6e5-764b-4de9-84ea-97abdee6b02f">IPropertyValue</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3675764D-7073-479B-8B9A-0AD037A963FB">GetUInt32</a>
</td>
<td align="left" width="63%">
Gets the unsigned 32-bit integer value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abea0460-73f1-4828-9cf7-d6bcad90f2ab">GetUInt32Array</a>
</td>
<td align="left" width="63%">
Gets the array of unsigned 32-bit integer values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2FD209CA-9A8D-40F3-B82E-E80A7D212A5D">GetUInt64</a>
</td>
<td align="left" width="63%">
Gets the unsigned 64-bit integer value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2981b2dc-d3ec-4886-a191-4dade13c7f32">GetUInt64Array</a>
</td>
<td align="left" width="63%">
Gets the array of unsigned 64-bit integer values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/736B44FF-F5A7-463A-9892-399CB3EC90B4">GetUInt8</a>
</td>
<td align="left" width="63%">
Gets the unsigned 8-bit integer value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f17fe310-40b7-46a5-ae87-c07649c2f288">GetUInt8Array</a>
</td>
<td align="left" width="63%">
Gets the array of unsigned 8-bit integer values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyValue</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8C6C042A-53AA-439B-8D8D-F67DB45CC3C6">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the data type of the value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>



<a href="https://msdn.microsoft.com/A4DC4348-88EE-48FB-91ED-F1D12FC89EE1">PropertyType</a>
 

 

