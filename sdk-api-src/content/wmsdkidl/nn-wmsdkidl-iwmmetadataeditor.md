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



The <b>IWMMetadataEditor</b> interface is used to edit metadata information in ASF file headers. It is obtained by calling the <a href="https://msdn.microsoft.com/en-us/library/Dd757753(v=VS.85).aspx">WMCreateEditor</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMMetadataEditor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMMetadataEditor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd757235(v=VS.85).aspx">Close</a>
</td>
<td align="left" width="63%">
Closes the currently open file without writing any changes to the metadata back to the disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757236(v=VS.85).aspx">Flush</a>
</td>
<td align="left" width="63%">
Closes the currently open file, writing any changes to the metadata back to the disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757237(v=VS.85).aspx">Open</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd798279(v=VS.85).aspx">IWMDRMEditor</a>
</td>
<td>IID_IWMDRMEditor</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd798504(v=VS.85).aspx">IWMHeaderInfo</a>
</td>
<td>IID_IWMHeaderInfo</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd798505(v=VS.85).aspx">IWMHeaderInfo2</a>
</td>
<td>IID_IWMHeaderInfo2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd798508(v=VS.85).aspx">IWMHeaderInfo3</a>
</td>
<td>IID_IWMHeaderInfo3</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757233(v=VS.85).aspx">IWMMetadataEditor2</a>
</td>
<td>IID_IWMMetadataEditor2</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/224eea1c-1d0d-47ac-9d99-c13674284f6d">Metadata Editor Object</a>
 

 

