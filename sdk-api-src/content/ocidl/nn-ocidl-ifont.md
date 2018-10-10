---
UID: NN:ocidl.IFont
title: IFont
author: windows-sdk-content
description: Provides a wrapper around a Windows font object.
old-location: com\ifont.htm
tech.root: com
ms.assetid: 3a04d2b7-b2eb-4c6c-8863-1e88321fa382
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: IFont, IFont interface [COM], IFont interface [COM],described, _ctrl_ifont, com.ifont, ocidl/IFont
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFont interface


## -description


Provides a wrapper around a Windows font object. The COM font object supports a number of 
    read/write properties as well as a set of methods through its <b>IFont</b> 
    interface. It supports the same set of properties (but not the methods) through the dispatch interface 
    <a href="https://msdn.microsoft.com/c2ee251e-2419-4436-96e4-caaf6acc2550">IFontDisp</a>, which is derived from 
    <b>IDispatch</b> to provide access to the font's properties through Automation. The system 
    provides a standard implementation of the font object with both interfaces.

The font object also supports the outgoing interface 
    <a href="https://msdn.microsoft.com/bfdf315c-6375-4c77-abd8-03f07342820f">IPropertyNotifySink</a> so a client can determine when 
    font properties change. Because the font object supports at least one outgoing interface, it also implements 
    <a href="https://msdn.microsoft.com/5e2be055-7baa-4c42-bd20-b338da296ab0">IConnectionPointContainer</a> and related interfaces 
    for this purpose.

The font object provides an hFont property, which is a Windows font handle that 
    conforms to the other attributes specified for the font. The font object delays realizing this 
    hFont object when possible, so consecutively setting two properties on a font 
    will not cause an intermediate font to be realized. In addition, as an optimization, the system-implemented font 
    object maintains a cache of font handles. Two font objects in the same process that have identical properties will 
    return the same font handle. The font object can remove font handles from this cache at will, which introduces 
    special considerations for clients using the hFont property.

The font object also supports <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a> so that it 
    can save and load itself from an instance of <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>. An object 
    that uses a font object internally would normally save and load the font as part of the object's own persistence 
    handling.

In addition, the font object supports <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>, which can 
    render a property set containing the font's attributes, allowing a client to save these properties as text.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFont</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IFont</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFont</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f86d52b8-e763-4948-b853-039721ae9b38">AddRefHfont</a>
</td>
<td align="left" width="63%">
Notifies the font object that the previously realized font identified with 
       hFont (from 
       <a href="https://msdn.microsoft.com/19bfd78a-0e81-45c3-a3b8-bc893669e9f5">get_hFont</a>) should remain valid until 
       <a href="https://msdn.microsoft.com/2c2cf2e0-d0c8-4e4f-ba5a-6b08650aee68">ReleaseHfont</a> is called or the font object itself is 
       released.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de5da0d1-338a-455c-a04b-99dc025b95bb">Clone</a>
</td>
<td align="left" width="63%">
Creates a duplicate font object with a state identical to the current font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc0a8353-852b-4314-83b1-a07321159945">get_Bold</a>
</td>
<td align="left" width="63%">
Gets the font's current Bold property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a784453-db29-4917-90ee-8893f787646a">get_Charset</a>
</td>
<td align="left" width="63%">
Retrieves the character set used in the font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19bfd78a-0e81-45c3-a3b8-bc893669e9f5">get_hFont</a>
</td>
<td align="left" width="63%">
Retrieves a handle to the font described by this font object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d56c21d6-1296-4c0c-a13e-8e4b3164e747">get_Italic</a>
</td>
<td align="left" width="63%">
Gets the font's current Italic property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04ce50a6-b833-4476-91a9-0d1ca7296314">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the name of the font family.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aeee7dfc-5ccd-4c30-a59e-5eec93505288">get_Size</a>
</td>
<td align="left" width="63%">
Retrieves the point size of the font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e70ea85a-fc76-412c-a100-c834dc8f0208">get_Strikethrough</a>
</td>
<td align="left" width="63%">
Gets the font's current Strikethrough property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/714a2678-6e3d-4b8d-8632-20eb41618fff">get_Underline</a>
</td>
<td align="left" width="63%">
Gets the font's current Underline property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3dad6648-752d-48f8-9267-24a5f5b0346c">get_Weight</a>
</td>
<td align="left" width="63%">
Gets the font's current Weight property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/becef75d-8342-4b4f-82e2-f1cca4eb619e">IsEqual</a>
</td>
<td align="left" width="63%">
Compares this font object to another for equality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c25738fe-daf4-4eac-b4b0-354950e29f27">put_Bold</a>
</td>
<td align="left" width="63%">
Sets the font's Bold property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da48fefa-28d2-41aa-a324-dc259504c9ed">put_Charset</a>
</td>
<td align="left" width="63%">
Sets the font's character set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a59169e1-d3c4-4dc0-b228-afad0e4d4307">put_Italic</a>
</td>
<td align="left" width="63%">
Sets the font's Italic property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3593d5c9-e2b7-4d85-b8f7-94f01a901030">put_Name</a>
</td>
<td align="left" width="63%">
Specifies a new name for the font family.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c39a7dc-553b-41b7-8b66-1a5980493dce">put_Size</a>
</td>
<td align="left" width="63%">
Sets the point size of the font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32b9c3aa-4c89-441e-9b41-0ac6d8a52bba">put_Strikethrough</a>
</td>
<td align="left" width="63%">
Sets the font's Strikethrough property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c763c050-cf69-4c9d-83a9-66ccc1d4376c">put_Underline</a>
</td>
<td align="left" width="63%">
Sets the font's Underline property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/716c77f3-6224-40d7-abea-46ed5eedb08a">put_Weight</a>
</td>
<td align="left" width="63%">
Sets the font's Weight property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/960dcc0b-8769-415c-9d5a-eaf9f4b3aeac">QueryTextMetrics</a>
</td>
<td align="left" width="63%">
Retrieves information about the font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c2cf2e0-d0c8-4e4f-ba5a-6b08650aee68">ReleaseHfont</a>
</td>
<td align="left" width="63%">
Notifies the font object that the caller that previously locked this font in the cache with 
       <a href="https://msdn.microsoft.com/f86d52b8-e763-4948-b853-039721ae9b38">AddRefHfont</a> no longer requires the lock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/daba0cfa-1628-415a-8161-75f7edfeeca8">SetHdc</a>
</td>
<td align="left" width="63%">
Provides a device context handle to the font that describes the logical mapping mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aaa962d8-6f7f-4031-aa10-09cadf0e5aec">SetRatio</a>
</td>
<td align="left" width="63%">
Converts the scaling factor for this font between logical units and <b>HIMETRIC</b> 
       units (in which is expressed the point size in the <b>Size</b> property).

</td>
</tr>
</table> 


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
<a href="https://msdn.microsoft.com/04ce50a6-b833-4476-91a9-0d1ca7296314">get_Name</a>
</td>
<td>
<a href="https://msdn.microsoft.com/3593d5c9-e2b7-4d85-b8f7-94f01a901030">put_Name</a>
</td>
<td>The facename of the font, e.g. Arial.</td>
</tr>
<tr>
<td><b>Size</b></td>
<td><b>CY</b></td>
<td>
<a href="https://msdn.microsoft.com/aeee7dfc-5ccd-4c30-a59e-5eec93505288">get_Size</a>
</td>
<td>
<a href="https://msdn.microsoft.com/1c39a7dc-553b-41b7-8b66-1a5980493dce">put_Size</a>
</td>
<td>The point size of the font, expressed in a <b>CY</b> type to allow for fractional 
       point sizes.</td>
</tr>
<tr>
<td><b>Bold</b></td>
<td><b>BOOL</b></td>
<td>
<a href="https://msdn.microsoft.com/bc0a8353-852b-4314-83b1-a07321159945">get_Bold</a>
</td>
<td>
<a href="https://msdn.microsoft.com/c25738fe-daf4-4eac-b4b0-354950e29f27">put_Bold</a>
</td>
<td>Indicates whether the font is boldfaced.</td>
</tr>
<tr>
<td><b>Italic</b></td>
<td><b>BOOL</b></td>
<td>
<a href="https://msdn.microsoft.com/d56c21d6-1296-4c0c-a13e-8e4b3164e747">get_Italic</a>
</td>
<td>
<a href="https://msdn.microsoft.com/a59169e1-d3c4-4dc0-b228-afad0e4d4307">put_Italic</a>
</td>
<td>Indicates whether the font is italicized.</td>
</tr>
<tr>
<td><b>Underline</b></td>
<td><b>BOOL</b></td>
<td>
<a href="https://msdn.microsoft.com/714a2678-6e3d-4b8d-8632-20eb41618fff">get_Underline</a>
</td>
<td>
<a href="https://msdn.microsoft.com/c763c050-cf69-4c9d-83a9-66ccc1d4376c">put_Underline</a>
</td>
<td>Indicates whether the font is underlined.</td>
</tr>
<tr>
<td><b>Strikethrough</b></td>
<td><b>BOOL</b></td>
<td>
<a href="https://msdn.microsoft.com/e70ea85a-fc76-412c-a100-c834dc8f0208">get_Strikethrough</a>
</td>
<td>
<a href="https://msdn.microsoft.com/32b9c3aa-4c89-441e-9b41-0ac6d8a52bba">put_Strikethrough</a>
</td>
<td>Indicates whether the font is strikethrough.</td>
</tr>
<tr>
<td><b>Weight</b></td>
<td><b>short</b></td>
<td>
<a href="https://msdn.microsoft.com/3dad6648-752d-48f8-9267-24a5f5b0346c">get_Weight</a>
</td>
<td>
<a href="https://msdn.microsoft.com/716c77f3-6224-40d7-abea-46ed5eedb08a">put_Weight</a>
</td>
<td>The boldness of the font.</td>
</tr>
<tr>
<td><b>Charset</b></td>
<td><b>short</b></td>
<td>
<a href="https://msdn.microsoft.com/3a784453-db29-4917-90ee-8893f787646a">get_Charset</a>
</td>
<td>
<a href="https://msdn.microsoft.com/da48fefa-28d2-41aa-a324-dc259504c9ed">put_Charset</a>
</td>
<td>The character set used in the font, such as <b>ANSI_CHARSET</b>, 
       <b>DEFAULT_CHARSET</b>, or <b>SYMBOL_CHARSET</b>.</td>
</tr>
<tr>
<td><b>hFont</b></td>
<td><b>HFONT</b></td>
<td>
<a href="https://msdn.microsoft.com/19bfd78a-0e81-45c3-a3b8-bc893669e9f5">get_hFont</a>
</td>
<td></td>
<td>The Windows font handle that can be selected into a device context for rendering.</td>
</tr>
</table>
 

<h3><a id="OLE_Implementation"></a><a id="ole_implementation"></a><a id="OLE_IMPLEMENTATION"></a>OLE Implementation</h3>
The system provides a standard implementation of a font object with the 
      <b>IFont</b> interface on top of the underlying system font support. A 
      font object is created through the function 
      <a href="https://msdn.microsoft.com/9ab384d6-fc21-4152-a0cf-744948f2f72c">OleCreateFontIndirect</a>. A font object supports a 
      number of read/write properties as well as a set of methods through its 
      <b>IFont</b> interface and supports the same set of properties (but not 
      the methods) through a dispatch interface <a href="https://msdn.microsoft.com/c2ee251e-2419-4436-96e4-caaf6acc2550">IFontDisp</a> which is 
      derived from <b>IDispatch</b> to provide access to the font's properties through 
      Automation. The system implementation of the font object supplies both interfaces.




## -see-also




<a href="https://msdn.microsoft.com/c2ee251e-2419-4436-96e4-caaf6acc2550">IFontDisp</a>
 

 

