---
UID: NN:windows.foundation.IPropertyValueStatics
title: IPropertyValueStatics (windows.foundation.h)
author: windows-sdk-content
description: Creates IPropertyValue objects that you can store in a property store.
old-location: winrt\ipropertyvaluestatics.htm
tech.root: WinRT
ms.assetid: 946BD4F9-318C-4452-AEDB-DF2212A2D3CA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPropertyValueStatics, IPropertyValueStatics interface [Windows Runtime], IPropertyValueStatics interface [Windows Runtime],described, windows/IPropertyValueStatics, winrt.ipropertyvaluefactory, winrt.ipropertyvaluestatics
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
 - IPropertyValueStatics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValueStatics interface


## -description


Creates <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> objects that you can store in a property store.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyValueStatics</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>. <b>IPropertyValueStatics</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyValueStatics</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F825D8F2-8FCE-48A7-9BD8-57E5D97A0E88">CreateBoolean</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified 8-bit Boolean value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54289d10-8393-4c49-9087-873519b32aa8">CreateBooleanArray</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of 8-bit Boolean values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E8400B85-029A-4E9A-963B-CC3012B7BE7F">CreateChar16</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified Unicode character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d78015a-dfe1-49be-8523-a5b0f96f7c58">CreateChar16Array</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of Unicode characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7191a38-df9e-4e19-a128-35260bbbfba9">CreateDateTime</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified <a href="https://msdn.microsoft.com/b5533002-8a72-438d-a3d3-0902ffc21830">DateTime</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c0beb76-0089-46b9-bcc5-ed07320859a3">CreateDateTimeArray</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of <a href="https://msdn.microsoft.com/b5533002-8a72-438d-a3d3-0902ffc21830">DateTime</a> values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66BB900A-797A-4589-AB9F-C35371F2671E">CreateDouble</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified 64-bit floating point value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/709235a3-0699-49a2-a487-76bc5e4efb64">CreateDoubleArray</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of 64-bit floating point values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B1189E10-BB04-4648-87F9-447026E441D8">CreateEmpty</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that represents an empty value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb895839-953f-41e2-963a-26156c490df0">CreateGuid</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified <b>GUID</b> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8284b582-2bba-4afd-9f8c-3b2169e0adbf">CreateGuidArray</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of <a href="https://msdn.microsoft.com/library/system.guid.aspx">Guid</a> values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6FCAD9E9-AB44-4D26-BD75-26B1C25FA524">CreateInspectable</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bcb8530-07cb-4f54-b727-e08807c3f22b">CreateInspectableArray</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of  <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E6F3751A-54FF-44EC-90EB-4B0732ABFF01">CreateInt32</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified signed 32-bit integer value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/148eae0c-db3b-4a62-8edb-3225a688265c">CreateInt32Array</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of signed 32-bit integer values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70533BB7-E844-459C-ACA3-D76142B379F4">CreateInt64</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified signed 64-bit integer value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c226a049-e8e5-4283-a8c4-102beed08b23">CreateInt64Array</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of signed 64-bit integer values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4cf8b1b-1673-4ac0-a66d-d83b98eec741">CreatePoint</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified <a href="https://msdn.microsoft.com/0cdd5b17-2f7e-4e17-896c-7d7784c8643d">Point</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdfc2a91-0f1b-41d9-99e3-e3589bdae6ca">CreatePointArray</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of <a href="https://msdn.microsoft.com/0cdd5b17-2f7e-4e17-896c-7d7784c8643d">Point</a> values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2938c3e0-6383-4136-99a6-c47a04c331f7">CreateRect</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified <a href="https://msdn.microsoft.com/420daab1-71e7-4610-b454-a49a64061f97">Rect</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/945f9c0a-22fe-42f6-b29b-3260607345f7">CreateRectArray</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of <a href="https://msdn.microsoft.com/420daab1-71e7-4610-b454-a49a64061f97">Rect</a> values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A74F66F8-3F02-4CD0-86BC-FBEC340466C4">CreateSingle</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified 32-bit floating point value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/525303cc-052b-4895-92a6-cfb5985b31d2">CreateSingleArray</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of 32-bit floating point values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a5055f1-6873-4396-9a3e-b7a4cc41200e">CreateSize</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified <a href="https://msdn.microsoft.com/8705adcb-a657-4b47-94ba-632bfb3779be">Size</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b9916e7-0a0d-44b1-8f8d-8307c145e57a">CreateSizeArray</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of <a href="https://msdn.microsoft.com/8705adcb-a657-4b47-94ba-632bfb3779be">Size</a> values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09622009-3E53-4ACD-99AE-83EA20FC55D9">CreateString</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified string value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9741a88-4585-4eda-b21d-5af0e541ef48">CreateStringArray</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of string values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eae11d63-c909-45fc-a38f-d9599b873b6f">CreateTimeSpan</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified <a href="https://msdn.microsoft.com/fbc6ecc2-6372-4b15-9532-3cd68a72e7b4">TimeSpan</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f663acc-5ced-4fd2-a0d5-3e462fe60251">CreateTimeSpanArray</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of <a href="https://msdn.microsoft.com/fbc6ecc2-6372-4b15-9532-3cd68a72e7b4">TimeSpan</a> values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E2ABD665-0BBD-4EA3-A265-D5EB12667F0A">CreateUInt32</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified unsigned 32-bit integer value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f56b855-a116-4c58-ae93-1a3d49240685">CreateUInt32Array</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of unsigned 32-bit integer values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49158177-D74E-4310-984D-A1C511840EF9">CreateUInt64</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified unsigned 64-bit integer value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b159f49-ce0e-4e68-ab13-f6d84af63ebf">CreateUInt64Array</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of unsigned 64-bit integer values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8CDCDB96-7E77-4B63-8417-D669ED4850BF">CreateUInt8</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified unsigned 8-bit integer value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc666379-4992-47da-b97b-b296219e26c1">CreateUInt8Array</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified array of unsigned 8-bit integer values.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>



<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>
 

 

