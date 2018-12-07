---
UID: NN:imapi2fs.IFsiFileItem
title: IFsiFileItem
author: windows-sdk-content
description: Use this interface to identify the file size and data stream of the file contents.
old-location: imapi\ifsifileitem.htm
tech.root: imapi
ms.assetid: 13085b1f-4ff9-48ff-a9ae-9a1c5cb9a108
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsiFileItem, IFsiFileItem interface [IMAPI], IFsiFileItem interface [IMAPI],described, imapi.ifsifileitem, imapi2fs/IFsiFileItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - imapi2fs.h
api_name:
 - IFsiFileItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsiFileItem interface


## -description


Use this interface to identify the file size and data stream of the file contents.

To get this interface, call the <a href="https://msdn.microsoft.com/8e90e367-e7c3-41db-a8c9-9b0220cf402b">IFileSystemImage::CreateFileItem</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsiFileItem</b> interface inherits from <a href="https://msdn.microsoft.com/44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0">IFsiItem</a>. <b>IFsiFileItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsiFileItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90ed4c81-7113-4329-ae1e-9114740b7e09">get_Data</a>
</td>
<td align="left" width="63%">
Retrieves the data stream of the file's content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0e53ca9-bb72-4191-9025-d07030c59a51">get_DataSize</a>
</td>
<td align="left" width="63%">
Retrieves the number of bytes in the file. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f4f06e7-10a6-4aa0-b7b1-bf8799fcd41e">get_DataSize32BitHigh</a>
</td>
<td align="left" width="63%">
Retrieves the most significant 32 bits of the <a href="https://msdn.microsoft.com/e0e53ca9-bb72-4191-9025-d07030c59a51">get_DataSize</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/beeec2bc-5f0e-4a53-afed-50c0b6069f54">get_DataSize32BitLow</a>
</td>
<td align="left" width="63%">
Retrieves the least significant 32 bits of the <a href="https://msdn.microsoft.com/e0e53ca9-bb72-4191-9025-d07030c59a51">get_DataSize</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fe00500-615c-48fe-a4a3-b3291e61db1f">put_Data</a>
</td>
<td align="left" width="63%">
Sets the data stream of the file's content.

</td>
</tr>
</table> 


## -remarks



Data streams for files contained within the file system image are read-only.  File data can only be replaced by overwriting an existing file item.

This is an <b>FsiFileItem</b> object in script.




## -see-also




<a href="https://msdn.microsoft.com/44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0">IFsiItem</a>
 

 

