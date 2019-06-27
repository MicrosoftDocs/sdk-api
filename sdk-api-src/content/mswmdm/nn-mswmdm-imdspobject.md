---
UID: NN:mswmdm.IMDSPObject
title: IMDSPObject (mswmdm.h)
author: windows-sdk-content
description: The IMDSPObject interface manages the transfer of data to and from storage media.The Open, Read, Write, and Close methods are valid only if the storage object is a file.
old-location: wmdm\imdspobject.htm
tech.root: WMDM
ms.assetid: 271d7185-1a9d-4bec-9289-4ae5461ed741
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPObject, IMDSPObject interface [windows Media Device Manager], IMDSPObject interface [windows Media Device Manager],described, IMDSPObjectInterface, mswmdm/IMDSPObject, wmdm.imdspobject
ms.topic: interface
f1_keywords: 
 - "mswmdm/IMDSPObject"
req.header: mswmdm.h
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
 - mswmdm.h
api_name:
 - IMDSPObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPObject interface


## -description



The <b>IMDSPObject</b> interface manages the transfer of data to and from storage media.

The <b>Open</b>, <b>Read</b>, <b>Write</b>, and <b>Close</b> methods are valid only if the storage object is a file. The client would typically call <b>Open</b>, perform a number of <b>Read</b> or <b>Write</b> operations and then call <b>Close</b>. This allows for a buffered mode read/write of the storage medium. The service provider should be able to handle any other calls on the device or storage interfaces (for example, enumerating content or getting global information about the storage medium) while the read or write operation is in progress.

The service provider should also be able to handle simultaneous read or write operations on multiple files. If the underlying file-system does not support opening of multiple files at the same time, service provider should gracefully return an error.

The <b>Delete</b>, <b>Rename</b>, and <b>Move</b> methods are valid for both files and folders.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-close">Close</a>
</td>
<td align="left" width="63%">
Closes a file on a storage medium of a media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes an object from a storage medium on a media device. This object can be either a file or a folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-move">Move</a>
</td>
<td align="left" width="63%">
Moves an object on a media device. This object can be either a file or a folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-open">Open</a>
</td>
<td align="left" width="63%">
Opens the associated object and prepares it for other operations. This object must be a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read">Read</a>
</td>
<td align="left" width="63%">
Reads data from the object at the current position. This object must be a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-rename">Rename</a>
</td>
<td align="left" width="63%">
Renames the associated object. This object can be either a file or a folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-seek">Seek</a>
</td>
<td align="left" width="63%">
Sets the current position within the object. This object must be a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write">Write</a>
</td>
<td align="left" width="63%">
Writes data to the object at the current position within the object. This object must be a file.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2">IMDSPObject2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
 

 

