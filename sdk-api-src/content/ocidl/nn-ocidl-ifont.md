---
UID: NN:ocidl.IFont
title: IFont (ocidl.h)
description: Provides a wrapper around a Windows font object.
helpviewer_keywords: ["IFont","IFont interface [COM]","IFont interface [COM]","described","_ctrl_ifont","com.ifont","ocidl/IFont"]
old-location: com\ifont.htm
tech.root: com
ms.assetid: 3a04d2b7-b2eb-4c6c-8863-1e88321fa382
ms.date: 12/05/2018
ms.keywords: IFont, IFont interface [COM], IFont interface [COM],described, _ctrl_ifont, com.ifont, ocidl/IFont
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFont
 - ocidl/IFont
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont
---

# IFont interface


## -description

Provides a wrapper around a Windows font object. The COM font object supports a number of 
    read/write properties as well as a set of methods through its <b>IFont</b> 
    interface. It supports the same set of properties (but not the methods) through the dispatch interface 
    <a href="/windows/desktop/api/ocidl/nn-ocidl-ifontdisp">IFontDisp</a>, which is derived from 
    <b>IDispatch</b> to provide access to the font's properties through Automation. The system 
    provides a standard implementation of the font object with both interfaces.

The font object also supports the outgoing interface 
    <a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertynotifysink">IPropertyNotifySink</a> so a client can determine when 
    font properties change. Because the font object supports at least one outgoing interface, it also implements 
    <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> and related interfaces 
    for this purpose.

The font object provides an hFont property, which is a Windows font handle that 
    conforms to the other attributes specified for the font. The font object delays realizing this 
    hFont object when possible, so consecutively setting two properties on a font 
    will not cause an intermediate font to be realized. In addition, as an optimization, the system-implemented font 
    object maintains a cache of font handles. Two font objects in the same process that have identical properties will 
    return the same font handle. The font object can remove font handles from this cache at will, which introduces 
    special considerations for clients using the hFont property.

The font object also supports <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> so that it 
    can save and load itself from an instance of <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>. An object 
    that uses a font object internally would normally save and load the font as part of the object's own persistence 
    handling.

In addition, the font object supports <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, which can 
    render a property set containing the font's attributes, allowing a client to save these properties as text.

## -inheritance

The <b>IFont</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFont</b> also has these types of members:

## -remarks

Each property in the <b>IFont</b> interface includes a 
     <b>get_<i>PropertyName</i></b> method if the property supports read 
     access and a <b>put_<i>PropertyName</i></b> method if the property 
     supports write access. Most of these properties support both read and write access.

<table>
<tr>
<th>Property</th>
<th>Type</th>
<th>Read Access Method</th>
<th>Write Access Method</th>
<th>Description</th>
</tr>
<tr>
<td><b>Name</b></td>
<td><b>BSTR</b></td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_name">get_Name</a>
</td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_name">put_Name</a>
</td>
<td>The facename of the font, e.g. Arial.</td>
</tr>
<tr>
<td><b>Size</b></td>
<td><b>CY</b></td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_size">get_Size</a>
</td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_size">put_Size</a>
</td>
<td>The point size of the font, expressed in a <b>CY</b> type to allow for fractional 
       point sizes.</td>
</tr>
<tr>
<td><b>Bold</b></td>
<td><b>BOOL</b></td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_bold">get_Bold</a>
</td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_bold">put_Bold</a>
</td>
<td>Indicates whether the font is boldfaced.</td>
</tr>
<tr>
<td><b>Italic</b></td>
<td><b>BOOL</b></td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_italic">get_Italic</a>
</td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_italic">put_Italic</a>
</td>
<td>Indicates whether the font is italicized.</td>
</tr>
<tr>
<td><b>Underline</b></td>
<td><b>BOOL</b></td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_underline">get_Underline</a>
</td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_underline">put_Underline</a>
</td>
<td>Indicates whether the font is underlined.</td>
</tr>
<tr>
<td><b>Strikethrough</b></td>
<td><b>BOOL</b></td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_strikethrough">get_Strikethrough</a>
</td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_strikethrough">put_Strikethrough</a>
</td>
<td>Indicates whether the font is strikethrough.</td>
</tr>
<tr>
<td><b>Weight</b></td>
<td><b>short</b></td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_weight">get_Weight</a>
</td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_weight">put_Weight</a>
</td>
<td>The boldness of the font.</td>
</tr>
<tr>
<td><b>Charset</b></td>
<td><b>short</b></td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_charset">get_Charset</a>
</td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_charset">put_Charset</a>
</td>
<td>The character set used in the font, such as <b>ANSI_CHARSET</b>, 
       <b>DEFAULT_CHARSET</b>, or <b>SYMBOL_CHARSET</b>.</td>
</tr>
<tr>
<td><b>hFont</b></td>
<td><b>HFONT</b></td>
<td>
<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_hfont">get_hFont</a>
</td>
<td></td>
<td>The Windows font handle that can be selected into a device context for rendering.</td>
</tr>
</table>
 

<h3><a id="OLE_Implementation"></a><a id="ole_implementation"></a><a id="OLE_IMPLEMENTATION"></a>OLE Implementation</h3>
The system provides a standard implementation of a font object with the 
      <b>IFont</b> interface on top of the underlying system font support. A 
      font object is created through the function 
      <a href="/windows/desktop/api/olectl/nf-olectl-olecreatefontindirect">OleCreateFontIndirect</a>. A font object supports a 
      number of read/write properties as well as a set of methods through its 
      <b>IFont</b> interface and supports the same set of properties (but not 
      the methods) through a dispatch interface <a href="/windows/desktop/api/ocidl/nn-ocidl-ifontdisp">IFontDisp</a> which is 
      derived from <b>IDispatch</b> to provide access to the font's properties through 
      Automation. The system implementation of the font object supplies both interfaces.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifontdisp">IFontDisp</a>
