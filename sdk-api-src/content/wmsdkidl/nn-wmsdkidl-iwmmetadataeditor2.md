---
UID: NN:wmsdkidl.IWMMetadataEditor2
title: IWMMetadataEditor2
author: windows-sdk-content
description: The IWMMetadataEditor2 interface provides an improved method for opening files for metadata operations.This interface is implemented as part of the metadata editor object.
old-location: wmformat\iwmmetadataeditor2.htm
tech.root: wmformat
ms.assetid: e991ac8e-35af-484f-8c60-dc6a7d402120
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMMetadataEditor2, IWMMetadataEditor2 interface [windows Media Format], IWMMetadataEditor2 interface [windows Media Format],described, IWMMetadataEditor2Interface, wmformat.iwmmetadataeditor2, wmsdkidl/IWMMetadataEditor2
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMMetadataEditor2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMMetadataEditor2 interface


## -description



The <b>IWMMetadataEditor2</b> interface provides an improved method for opening files for metadata operations.

This interface is implemented as part of the metadata editor object. To obtain a pointer to <b>IWMMetadataEditor2</b>, call the <b>QueryInterface</b> method of any other interface in an existing metadata editor object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMMetadataEditor2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd757232(v=VS.85).aspx">IWMMetadataEditor</a>. <b>IWMMetadataEditor2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMMetadataEditor2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757234(v=VS.85).aspx">OpenEx</a>
</td>
<td align="left" width="63%">
Opens a file so that the metadata can be accessed.

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
<a href="https://msdn.microsoft.com/en-us/library/Dd757232(v=VS.85).aspx">IWMMetadataEditor</a>
</td>
<td>IID_IWMMetadataEditor</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757232(v=VS.85).aspx">IWMMetadataEditor Interface</a>



<a href="https://msdn.microsoft.com/224eea1c-1d0d-47ac-9d99-c13674284f6d">Metadata Editor Object</a>
 

 

