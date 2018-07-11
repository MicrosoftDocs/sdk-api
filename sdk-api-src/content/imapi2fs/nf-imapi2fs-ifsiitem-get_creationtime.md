---
UID: NF:imapi2fs.IFsiItem.get_CreationTime
title: IFsiItem::get_CreationTime
author: windows-sdk-content
description: Retrieves the date and time that the directory or file item was created and added to the file system image.
old-location: imapi\ifsiitem_get_creationtime.htm
old-project: imapi
ms.assetid: c172bbed-6573-4b11-9aa6-9d4dde9cd94a
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: IFsiItem interface [IMAPI],get_CreationTime method, IFsiItem.get_CreationTime, IFsiItem::get_CreationTime, get_CreationTime, get_CreationTime method [IMAPI], get_CreationTime method [IMAPI],IFsiItem interface, imapi.ifsiitem_get_creationtime, imapi2fs/IFsiItem::get_CreationTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IFsiItem.get_CreationTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFsiItem::get_CreationTime


## -description


Retrieves the date and time that the directory or file item was created and added to the file system image.


## -parameters




### -param pVal [out]

Date and time that the  directory or file item was created and added to the file system image, according to UTC time. 


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -remarks



The creation date and time are propagated to the attributes that users see when listing the contents of a directory.

IMAPI does not support the extended attribute for <i>CreationTime</i>, and as a result, UDFS populates the <i>CreationTime</i> with the value expressed by the <i>LastAccessed</i> property from the file entry.




## -see-also




<a href="https://msdn.microsoft.com/44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0">IFsiItem</a>



<a href="https://msdn.microsoft.com/242e6f68-d9bc-4881-adf3-22d7b32a1dfe">IFsiItem::put_CreationTime</a>
 

 

