---
UID: NN:imapi2fs.IFsiItem
title: IFsiItem (imapi2fs.h)
author: windows-sdk-content
description: Base interface containing properties common to both file and directory items.
old-location: imapi\ifsiitem.htm
tech.root: imapi
ms.assetid: 44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsiItem, IFsiItem interface [IMAPI], IFsiItem interface [IMAPI],described, imapi.ifsiitem, imapi2fs/IFsiItem
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
 - IFsiItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsiItem interface


## -description


Base interface containing properties common to both file and directory items. 

To access the properties of this interface, use the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem">IFsiFileItem</a> or <a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsiItem</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsiItem</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-filesystemname">FileSystemName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the item as modified to conform to the specified file system. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-filesystempath">FileSystemPath</a>
</td>
<td align="left" width="63%">
Retrieves the full path of the item as modified to conform to the specified file system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-get_creationtime">get_CreationTime</a>
</td>
<td align="left" width="63%">
Retrieves the date and time that the item was created in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-get_fullpath">get_FullPath</a>
</td>
<td align="left" width="63%">
Retrieves the full path of the file or directory item in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-get_ishidden">get_IsHidden</a>
</td>
<td align="left" width="63%">
Determines if the item's hidden attribute is set in the file system image. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-get_lastaccessedtime">get_LastAccessedTime</a>
</td>
<td align="left" width="63%">
Retrieves the date and time that the item was last accessed in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-get_lastmodifiedtime">get_LastModifiedTime</a>
</td>
<td align="left" width="63%">
Retrieves the date and time that the item was last modified in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the name of a directory or file in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-put_creationtime">put_CreationTime</a>
</td>
<td align="left" width="63%">
Sets the date and time that a file or directory was added to the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-put_ishidden">put_IsHidden</a>
</td>
<td align="left" width="63%">
Determines if the item's hidden attribute is set in the file system image. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-put_lastaccessedtime">put_LastAccessedTime</a>
</td>
<td align="left" width="63%">
Sets the date and time that the item was last accessed in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-put_lastmodifiedtime">put_LastModifiedTime</a>
</td>
<td align="left" width="63%">
Sets the date and time that the item was last modified in the file system image.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem">IFsiFileItem</a>
 

 

