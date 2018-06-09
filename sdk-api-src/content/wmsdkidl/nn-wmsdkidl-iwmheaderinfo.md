---
UID: NN:wmsdkidl.IWMHeaderInfo
title: IWMHeaderInfo
author: windows-sdk-content
description: The IWMHeaderInfo interface sets and retrieves information in the header section of an ASF file.
old-location: wmformat\iwmheaderinfo.htm
old-project: wmformat
ms.assetid: 649f9a73-c70a-4524-b577-366ade969f2f
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWMHeaderInfo, IWMHeaderInfo interface [windows Media Format], IWMHeaderInfo interface [windows Media Format],described, IWMHeaderInfoInterface, wmformat.iwmheaderinfo, wmsdkidl/IWMHeaderInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - wmsdkidl.h
api_name:
 - IWMHeaderInfo
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMHeaderInfo interface


## -description



The <b>IWMHeaderInfo</b> interface sets and retrieves information in the header section of an ASF file. You can manipulate three types of header information by using the methods of this interface: metadata attributes, <a href="wmformat_glossary.htm">markers</a>, and script commands.

Metadata attributes are name/value pairs that describe or relate to the contents of the file. Typical metadata attributes contain information about the artist, title, and performance details of the content. The Windows Media Format SDK includes a large selection of predefined metadata attributes that you can use in your files. See <a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a> for a complete listing of predefined attributes. Additionally, you can create your own attributes.

The methods of <b>IWMHeaderInfo</b> that deal with metadata are somewhat limited. They cannot be used to create or access attributes containing more than 64 kilobytes of data. They are also limited to simple data types. Much more robust metadata support is provided through the <a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3</a> interface, which should be used for all new files.

Markers enable you to name specific locations in the file for easy access. Typically, markers are used to create a table of contents for a file, such as a list of scenes in a video file.

Script commands are name/value pairs containing information that your reading application will respond to programmatically. There are no script commands that are directly supported by the reader or the synchronous reader, but there are a few standard script commands supported by Windows Media Player. For more information about script commands, see the <a href="https://msdn.microsoft.com/be8a2d22-35cb-4b8d-ad00-e8a45bb85b39">Using Script Commands</a> section of this documentation.

The <b>IWMHeaderInfo</b> interface is implemented by the metadata editor object, the writer object, the reader object, and the synchronous reader object. To obtain a pointer to an instance, call the <b>QueryInterface</b> method of any other interface in the desired object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMHeaderInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMHeaderInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMHeaderInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfa111bb-7bbb-448a-b2db-d36637c01a52">AddMarker</a>
</td>
<td align="left" width="63%">
Adds a marker, consisting of a name and a specific time, to the ASF file header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e20644fb-077e-4eee-8802-6099002f3969">AddScript</a>
</td>
<td align="left" width="63%">
Adds a script, consisting of type and command strings, and a specific time, to the ASF file header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/905fdf2c-a398-457e-80e9-aac124301f99">GetAttributeByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptive attribute that is stored in the ASF file header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8941b989-f052-4e61-a64a-06748947fcf4">GetAttributeByName</a>
</td>
<td align="left" width="63%">
Returns a descriptive attribute that is stored in the ASF file header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5f0be62-4f15-45ca-8593-f5703a1f932a">GetAttributeCount</a>
</td>
<td align="left" width="63%">
Returns the number of attributes defined in the ASF file header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae035991-86c8-4ffc-b819-5a5ce81a980f">GetMarker</a>
</td>
<td align="left" width="63%">
Returns the name and time of a marker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0d8e61d-8703-407a-9610-9e9f29ab92a1">GetMarkerCount</a>
</td>
<td align="left" width="63%">
Returns the number of markers currently in the ASF file header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/779a7618-9f22-4caf-8a4e-b622e422c30d">GetScript</a>
</td>
<td align="left" width="63%">
Returns the type and command strings, and time of a script.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1a0b35c-db05-402a-9bde-684bead1eedf">GetScriptCount</a>
</td>
<td align="left" width="63%">
Returns the number of scripts currently in the ASF file header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b95aa113-b218-44ef-9516-20894e02ee6c">RemoveMarker</a>
</td>
<td align="left" width="63%">
Removes a marker from the ASF file header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c66e808d-25f9-4745-8bcc-731f2556f470">RemoveScript</a>
</td>
<td align="left" width="63%">
Removes a script from the ASF file header.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/174969a2-4fe2-477b-9990-051d23bf8a29">SetAttribute</a>
</td>
<td align="left" width="63%">
Sets a descriptive attribute that is stored in the ASF file header.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -remarks



Although the <b>IWMHeaderInfo</b> interface is accessible from four different objects, not all of the features are available in all cases. The following table summarizes the differences in implementation for the various objects.

<table>
<tr>
<th>
              Object
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>Metadata editor</td>
<td>Full functionality is implemented.</td>
</tr>
<tr>
<td>Writer</td>
<td>All methods that alter header items (those whose names begin with Add, Set, or Remove) are supported only before the <a href="https://msdn.microsoft.com/df511ff0-a87b-442a-85bd-c8d924ab2047">IWMWriter::BeginWriting</a> method is called.All marker methods return E_NOTIMPL.

</td>
</tr>
<tr>
<td>Reader and synchronous reader</td>
<td>All methods that alter header items (those whose names begin with Add, Set, or Remove) return E_NOTIMPL.</td>
</tr>
</table>
 

For information about using the writer for metadata editing, see <a href="https://msdn.microsoft.com/86badfe3-64bc-4285-a231-f6c0ebf4f262">To Edit Metadata with the Writer</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a>



<a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2 Interface</a>



<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3 Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/224eea1c-1d0d-47ac-9d99-c13674284f6d">Metadata Editor Object</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/52a4891f-03bf-4d8a-ab7b-e9739db30bc3">Synchronous Reader Object</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

