---
UID: NN:wmsdkidl.IWMMetadataEditor2
title: IWMMetadataEditor2
author: windows-sdk-content
description: The IWMMetadataEditor2 interface provides an improved method for opening files for metadata operations.This interface is implemented as part of the metadata editor object.
old-location: wmformat\iwmmetadataeditor2.htm
old-project: wmformat
ms.assetid: e991ac8e-35af-484f-8c60-dc6a7d402120
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWMMetadataEditor2, IWMMetadataEditor2 interface [windows Media Format], IWMMetadataEditor2 interface [windows Media Format],described, IWMMetadataEditor2Interface, wmformat.iwmmetadataeditor2, wmsdkidl/IWMMetadataEditor2
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
 - IWMMetadataEditor2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMMetadataEditor2 interface


## -description



The <b>IWMMetadataEditor2</b> interface provides an improved method for opening files for metadata operations.

This interface is implemented as part of the metadata editor object. To obtain a pointer to <b>IWMMetadataEditor2</b>, call the <b>QueryInterface</b> method of any other interface in an existing metadata editor object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMMetadataEditor2</b> interface inherits from <a href="https://msdn.microsoft.com/ad19cd3e-d1ef-4d6c-ac23-29a56e5c1d66">IWMMetadataEditor</a>. <b>IWMMetadataEditor2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e35f5f85-659e-4a1f-8bfd-4ad3e946d733">OpenEx</a>
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
<a href="https://msdn.microsoft.com/a404d30d-0b42-44c9-93e6-3eb9ef9e40fc">IWMDRMEditor</a>
</td>
<td>IID_IWMDRMEditor</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo</a>
</td>
<td>IID_IWMHeaderInfo</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2</a>
</td>
<td>IID_IWMHeaderInfo2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3</a>
</td>
<td>IID_IWMHeaderInfo3</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/ad19cd3e-d1ef-4d6c-ac23-29a56e5c1d66">IWMMetadataEditor</a>
</td>
<td>IID_IWMMetadataEditor</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ad19cd3e-d1ef-4d6c-ac23-29a56e5c1d66">IWMMetadataEditor Interface</a>



<a href="https://msdn.microsoft.com/224eea1c-1d0d-47ac-9d99-c13674284f6d">Metadata Editor Object</a>
 

 

