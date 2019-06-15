---
UID: NN:tuner.IComponentType
title: IComponentType (tuner.h)
author: windows-sdk-content
description: The IComponentType interface is implemented on ComponentType objects, and contains methods for setting and retrieving various properties for a Component.
old-location: mstv\icomponenttype.htm
tech.root: mstv
ms.assetid: e83bbbbe-64a9-4ed3-9c32-925ca80c2c38
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComponentType, IComponentType interface [Microsoft TV Technologies], IComponentType interface [Microsoft TV Technologies],described, IComponentTypeInterface, mstv.icomponenttype, tuner/IComponentType
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
ms.custom: 19H1
---

# IComponentType interface


## -description



The <b>IComponentType</b> interface is implemented on <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> objects, and contains methods for setting and retrieving various properties for a Component. Every Component object has an associated ComponentType object that is set or retrieved with the <b>get_Type</b> and <b>put_Type</b> methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponentType</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IComponentType</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of this component type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-get__mediaformattype">get__MediaFormatType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow media format type as a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-get__mediamajortype">get__MediaMajorType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow media major type as a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-get__mediasubtype">get__MediaSubType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow media subtype as a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-get_category">get_Category</a>
</td>
<td align="left" width="63%">
Retrieves the component category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-get_mediaformattype">get_MediaFormatType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow media format type as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-get_mediamajortype">get_MediaMajorType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow media major type as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-get_mediasubtype">get_MediaSubType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow media subtype as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-get_mediatype">get_MediaType</a>
</td>
<td align="left" width="63%">
Retrieves the DirectShow <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-_ammediatype">AM_MEDIA_TYPE</a> media type structure for the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-put__mediaformattype">put__MediaFormatType</a>
</td>
<td align="left" width="63%">
Sets the DirectShow media format type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-put__mediamajortype">put__MediaMajorType</a>
</td>
<td align="left" width="63%">
Sets the major type for the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-put__mediasubtype">put__MediaSubType</a>
</td>
<td align="left" width="63%">
Sets the subtype for the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-put_category">put_Category</a>
</td>
<td align="left" width="63%">
Sets the component category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-put_mediaformattype">put_MediaFormatType</a>
</td>
<td align="left" width="63%">
Sets the DirectShow media format type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-put_mediamajortype">put_MediaMajorType</a>
</td>
<td align="left" width="63%">
Sets the major type for the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-put_mediasubtype">put_MediaSubType</a>
</td>
<td align="left" width="63%">
Sets the subtype member for the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponenttype-put_mediatype">put_MediaType</a>
</td>
<td align="left" width="63%">
Sets the DirectShow <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-_ammediatype">AM_MEDIA_TYPE</a> media type structure for the component.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IComponentType)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

