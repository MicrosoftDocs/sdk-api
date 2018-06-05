---
UID: NF:imapi2fs.IFsiDirectoryItem.get_Count
title: IFsiDirectoryItem::get_Count
author: windows-sdk-content
description: Number of child items in the enumeration.
old-location: imapi\ifsidirectoryitem_get_count.htm
old-project: imapi
ms.assetid: 66553025-35c9-4902-a184-01c07a478977
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFsiDirectoryItem interface [IMAPI],get_Count method, IFsiDirectoryItem.get_Count, IFsiDirectoryItem::get_Count, get_Count, get_Count method [IMAPI], get_Count method [IMAPI],IFsiDirectoryItem interface, imapi.ifsidirectoryitem_get_count, imapi2fs/IFsiDirectoryItem::get_Count
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2fs.h
api_name:
-	IFsiDirectoryItem.get_Count
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFsiDirectoryItem::get_Count


## -description


Number of  child items in the enumeration.


## -parameters




### -param Count [out]

Number of directory and file items within the directory in the file system image.


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
 




## -see-also




<a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a>



<a href="https://msdn.microsoft.com/13085b1f-4ff9-48ff-a9ae-9a1c5cb9a108">IFsiFileItem</a>
 

 

