---
UID: NN:tuner.IComponentType
title: IComponentType
author: windows-sdk-content
description: The IComponentType interface is implemented on ComponentType objects, and contains methods for setting and retrieving various properties for a Component.
old-location: mstv\icomponenttype.htm
tech.root: mstv
ms.assetid: e83bbbbe-64a9-4ed3-9c32-925ca80c2c38
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IComponentType, IComponentType interface [Microsoft TV Technologies], IComponentType interface [Microsoft TV Technologies],described, IComponentTypeInterface, mstv.icomponenttype, tuner/IComponentType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IComponentType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponentType interface


## -description



The <b>IComponentType</b> interface is implemented on <a href="https://msdn.microsoft.com/d5d8af25-4d39-4327-bd6d-8984ae9e6a78">ComponentType</a> objects, and contains methods for setting and retrieving various properties for a Component. Every Component object has an associated ComponentType object that is set or retrieved with the <b>get_Type</b> and <b>put_Type</b> methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponentType</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IComponentType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComponentType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34cab0cb-8b38-4d03-be2a-ef14bd9505f2">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of this component type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21dccb42-8430-4fa0-a549-98dd3d1a4d4c">get__MediaFormatType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow media format type as a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8732070-3560-461b-a04e-3c00d6b7b49e">get__MediaMajorType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow media major type as a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92c49f9a-2102-424d-b04c-68aae8a37ada">get__MediaSubType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow media subtype as a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0a61359-a15a-47f6-8388-90368867e945">get_Category</a>
</td>
<td align="left" width="63%">
Retrieves the component category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b618f33-2ef8-420b-9a15-83e1899476bc">get_MediaFormatType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow media format type as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c1fc49d-acca-40fe-85cf-909092ceb5ef">get_MediaMajorType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow media major type as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/470b7960-b016-4807-858b-61a53daf2396">get_MediaSubType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow media subtype as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca13cfc0-3e51-41cd-9405-aaa96927a35c">get_MediaType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> media type structure for the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37baa69e-d942-41d6-b497-bf37d6b0d57b">put__MediaFormatType</a>
</td>
<td align="left" width="63%">
Sets the DirectShow media format type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3886f7fe-1520-4fee-a88b-26ee1cdf32fe">put__MediaMajorType</a>
</td>
<td align="left" width="63%">
Sets the major type for the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80b5e1d5-72e2-4523-86dd-88aff71a54db">put__MediaSubType</a>
</td>
<td align="left" width="63%">
Sets the subtype for the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ae90ec5-ebae-4a67-b786-33a1d94309b8">put_Category</a>
</td>
<td align="left" width="63%">
Sets the component category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfbf49a1-473b-4b51-ac35-a9ea982dcd7f">put_MediaFormatType</a>
</td>
<td align="left" width="63%">
Sets the DirectShow media format type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/455a51f4-eb01-437a-9cb9-6ff93a6cc76e">put_MediaMajorType</a>
</td>
<td align="left" width="63%">
Sets the major type for the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc635134-33da-4197-966a-5cb64315cb7c">put_MediaSubType</a>
</td>
<td align="left" width="63%">
Sets the subtype member for the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f77a391-232f-46ef-a028-763ebc706784">put_MediaType</a>
</td>
<td align="left" width="63%">
Sets the DirectShow <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> media type structure for the component.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IComponentType)</code>.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

