---
UID: NN:wmsdkidl.IWMMetadataEditor
title: IWMMetadataEditor (wmsdkidl.h)
author: windows-sdk-content
description: The IWMMetadataEditor interface is used to edit metadata information in ASF file headers. It is obtained by calling the WMCreateEditor function.
old-location: wmformat\iwmmetadataeditor.htm
tech.root: wmformat
ms.assetid: ad19cd3e-d1ef-4d6c-ac23-29a56e5c1d66
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMMetadataEditor, IWMMetadataEditor interface [windows Media Format], IWMMetadataEditor interface [windows Media Format],described, IWMMetadataEditorInterface, wmformat.iwmmetadataeditor, wmsdkidl/IWMMetadataEditor
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMMetadataEditor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMMetadataEditor interface


## -description



The <b>IWMMetadataEditor</b> interface is used to edit metadata information in ASF file headers. It is obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreateeditor">WMCreateEditor</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMMetadataEditor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMMetadataEditor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMMetadataEditor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmetadataeditor-close">Close</a>
</td>
<td align="left" width="63%">
Closes the currently open file without writing any changes to the metadata back to the disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmetadataeditor-flush">Flush</a>
</td>
<td align="left" width="63%">
Closes the currently open file, writing any changes to the metadata back to the disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmetadataeditor-open">Open</a>
</td>
<td align="left" width="63%">
Opens an ASF file.

</td>
</tr>
</table> 

The following interfaces can be obtained by using the QueryInterface method of this interface.

<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor">IWMDRMEditor</a>
</td>
<td>IID_IWMDRMEditor</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo</a>
</td>
<td>IID_IWMHeaderInfo</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2</a>
</td>
<td>IID_IWMHeaderInfo2</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a>
</td>
<td>IID_IWMHeaderInfo3</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2">IWMMetadataEditor2</a>
</td>
<td>IID_IWMMetadataEditor2</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>
 

 

