---
UID: NN:wmsdkidl.IWMHeaderInfo
title: IWMHeaderInfo (wmsdkidl.h)
description: The IWMHeaderInfo interface sets and retrieves information in the header section of an ASF file.
helpviewer_keywords: ["IWMHeaderInfo","IWMHeaderInfo interface [windows Media Format]","IWMHeaderInfo interface [windows Media Format]","described","IWMHeaderInfoInterface","wmformat.iwmheaderinfo","wmsdkidl/IWMHeaderInfo"]
old-location: wmformat\iwmheaderinfo.htm
tech.root: wmformat
ms.assetid: 649f9a73-c70a-4524-b577-366ade969f2f
ms.date: 4/26/2023
ms.keywords: IWMHeaderInfo, IWMHeaderInfo interface [windows Media Format], IWMHeaderInfo interface [windows Media Format],described, IWMHeaderInfoInterface, wmformat.iwmheaderinfo, wmsdkidl/IWMHeaderInfo
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMHeaderInfo
 - wmsdkidl/IWMHeaderInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMHeaderInfo
---

# IWMHeaderInfo interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMHeaderInfo</b> interface sets and retrieves information in the header section of an ASF file. You can manipulate three types of header information by using the methods of this interface: metadata attributes, <a href="/windows/desktop/wmformat/wmformat-glossary">markers</a>, and script commands.

Metadata attributes are name/value pairs that describe or relate to the contents of the file. Typical metadata attributes contain information about the artist, title, and performance details of the content. The Windows Media Format SDK includes a large selection of predefined metadata attributes that you can use in your files. See <a href="/windows/desktop/wmformat/attributes">Attributes</a> for a complete listing of predefined attributes. Additionally, you can create your own attributes.

The methods of <b>IWMHeaderInfo</b> that deal with metadata are somewhat limited. They cannot be used to create or access attributes containing more than 64 kilobytes of data. They are also limited to simple data types. Much more robust metadata support is provided through the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a> interface, which should be used for all new files.

Markers enable you to name specific locations in the file for easy access. Typically, markers are used to create a table of contents for a file, such as a list of scenes in a video file.

Script commands are name/value pairs containing information that your reading application will respond to programmatically. There are no script commands that are directly supported by the reader or the synchronous reader, but there are a few standard script commands supported by Windows Media Player. For more information about script commands, see the <a href="/windows/desktop/wmformat/using-script-commands">Using Script Commands</a> section of this documentation.

The <b>IWMHeaderInfo</b> interface is implemented by the metadata editor object, the writer object, the reader object, and the synchronous reader object. To obtain a pointer to an instance, call the <b>QueryInterface</b> method of any other interface in the desired object.

## -inheritance

The <b>IWMHeaderInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMHeaderInfo</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Although the <b>IWMHeaderInfo</b> interface is accessible from four different objects, not all of the features are available in all cases. The following table summarizes the differences in implementation for the various objects.

<table>
<tr>
<th>Object
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>Metadata editor</td>
<td>Full functionality is implemented.</td>
</tr>
<tr>
<td>Writer</td>
<td>All methods that alter header items (those whose names begin with Add, Set, or Remove) are supported only before the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a> method is called.All marker methods return E_NOTIMPL.

</td>
</tr>
<tr>
<td>Reader and synchronous reader</td>
<td>All methods that alter header items (those whose names begin with Add, Set, or Remove) return E_NOTIMPL.</td>
</tr>
</table>
 

For information about using the writer for metadata editing, see <a href="/windows/desktop/wmformat/to-edit-metadata-with-the-writer">To Edit Metadata with the Writer</a>.

## -see-also

<a href="/windows/desktop/wmformat/attributes">Attributes</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>
