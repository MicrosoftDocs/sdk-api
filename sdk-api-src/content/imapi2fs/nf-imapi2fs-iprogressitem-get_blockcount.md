---
UID: NF:imapi2fs.IProgressItem.get_BlockCount
title: IProgressItem::get_BlockCount
author: windows-sdk-content
description: Retrieves the number of blocks in the progress item.
old-location: imapi\iprogressitem_get_blockcount.htm
old-project: imapi
ms.assetid: 6960fecb-f202-4a10-9abb-fc945217a314
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: IProgressItem interface [IMAPI],get_BlockCount method, IProgressItem.get_BlockCount, IProgressItem::get_BlockCount, get_BlockCount, get_BlockCount method [IMAPI], get_BlockCount method [IMAPI],IProgressItem interface, imapi.iprogressitem_get_blockcount, imapi2fs/IProgressItem::get_BlockCount
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
 - IProgressItem.get_BlockCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IProgressItem::get_BlockCount


## -description


Retrieves the number of blocks in the progress item.


## -parameters




### -param blocks [out]

Number of blocks in the segment.


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




<a href="https://msdn.microsoft.com/b6ba9226-655e-4eac-ad43-2b5a8e90039f">IProgressItem</a>



<a href="https://msdn.microsoft.com/9c1c5932-0301-4752-871d-609d3c128906">IProgressItem::get_FirstBlock</a>



<a href="https://msdn.microsoft.com/ad75e708-4a10-45b9-89c2-11270f6edd9e">IProgressItem::get_LastBlock</a>
 

 

