---
UID: NN:imapi2fs.IFsiItem
title: IFsiItem
author: windows-sdk-content
description: Base interface containing properties common to both file and directory items.
old-location: imapi\ifsiitem.htm
old-project: imapi
ms.assetid: 44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IFsiItem, IFsiItem interface [IMAPI], IFsiItem interface [IMAPI],described, imapi.ifsiitem, imapi2fs/IFsiItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: imapi2fs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PlatformId
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFsiItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFsiItem interface


## -description


Base interface containing properties common to both file and directory items. 

To access the properties of this interface, use the <a href="https://msdn.microsoft.com/13085b1f-4ff9-48ff-a9ae-9a1c5cb9a108">IFsiFileItem</a> or <a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsiItem</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsiItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsiItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a10d9ee1-c05f-4e76-a921-af562dc68121">FileSystemName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the item as modified to conform to the specified file system. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6b969e2-9b1c-402e-81ea-ced13fca4551">FileSystemPath</a>
</td>
<td align="left" width="63%">
Retrieves the full path of the item as modified to conform to the specified file system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c172bbed-6573-4b11-9aa6-9d4dde9cd94a">get_CreationTime</a>
</td>
<td align="left" width="63%">
Retrieves the date and time that the item was created in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb2d6f13-a833-42a3-abbd-39f86b95082d">get_FullPath</a>
</td>
<td align="left" width="63%">
Retrieves the full path of the file or directory item in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1aec5bbc-d602-40c1-80e4-cad9dd8a2ab5">get_IsHidden</a>
</td>
<td align="left" width="63%">
Determines if the item's hidden attribute is set in the file system image. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e12f4c62-2dc8-4155-9cd7-0dea982d7b5a">get_LastAccessedTime</a>
</td>
<td align="left" width="63%">
Retrieves the date and time that the item was last accessed in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec7a3b44-817c-4420-81d5-61905aa4f2cf">get_LastModifiedTime</a>
</td>
<td align="left" width="63%">
Retrieves the date and time that the item was last modified in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cb6e270-6bbf-414f-a9ed-b290da3dafe9">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the name of a directory or file in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/242e6f68-d9bc-4881-adf3-22d7b32a1dfe">put_CreationTime</a>
</td>
<td align="left" width="63%">
Sets the date and time that a file or directory was added to the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a437daea-af30-43e5-bb88-e59de8ba37c9">put_IsHidden</a>
</td>
<td align="left" width="63%">
Determines if the item's hidden attribute is set in the file system image. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6192bff5-9535-4845-9c99-d5ceeea0335f">put_LastAccessedTime</a>
</td>
<td align="left" width="63%">
Sets the date and time that the item was last accessed in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11491b16-0bdc-41a6-a99d-0543cdc3bb64">put_LastModifiedTime</a>
</td>
<td align="left" width="63%">
Sets the date and time that the item was last modified in the file system image.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a>



<a href="https://msdn.microsoft.com/13085b1f-4ff9-48ff-a9ae-9a1c5cb9a108">IFsiFileItem</a>
 

 

