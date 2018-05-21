---
UID: NF:imapi2fs.IFsiFileItem.put_Data
title: IFsiFileItem::put_Data
author: windows-driver-content
description: Sets the data stream of the file's content.
old-location: imapi\ifsifileitem_put_data.htm
old-project: imapi
ms.assetid: 5fe00500-615c-48fe-a4a3-b3291e61db1f
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IFsiFileItem interface [IMAPI],put_Data method, IFsiFileItem.put_Data, IFsiFileItem::put_Data, imapi.ifsifileitem_put_data, imapi2fs/IFsiFileItem::put_Data, put_Data, put_Data method [IMAPI], put_Data method [IMAPI],IFsiFileItem interface
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2fs.h
api_name:
-	IFsiFileItem.put_Data
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFsiFileItem::put_Data


## -description


Sets the data stream of the file's content.


## -parameters




### -param newVal [in]

An <b>IStream</b> interface of the content of the file to add to the file system image. 


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
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
FileSystemImage object is in read only mode.

Value: 0xC0AAB102

</td>
</tr>
</table>
 




## -remarks



The contents of the file becomes read-only once the file item is added to file system image.




## -see-also




<a href="https://msdn.microsoft.com/13085b1f-4ff9-48ff-a9ae-9a1c5cb9a108">IFsiFileItem</a>



<a href="https://msdn.microsoft.com/90ed4c81-7113-4329-ae1e-9114740b7e09">IFsiFileItem::get_Data</a>
 

 

