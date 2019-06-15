---
UID: NF:imapi2fs.IFsiFileItem.get_DataSize
title: IFsiFileItem::get_DataSize (imapi2fs.h)
author: windows-sdk-content
description: Retrieves the number of bytes in the file.
old-location: imapi\ifsifileitem_get_datasize.htm
tech.root: imapi
ms.assetid: e0e53ca9-bb72-4191-9025-d07030c59a51
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsiFileItem interface [IMAPI],get_DataSize method, IFsiFileItem.get_DataSize, IFsiFileItem::get_DataSize, get_DataSize, get_DataSize method [IMAPI], get_DataSize method [IMAPI],IFsiFileItem interface, imapi.ifsifileitem_get_datasize, imapi2fs/IFsiFileItem::get_DataSize
ms.topic: method
f1_keywords: ["imapi2fs/IFsiFileItem.get_DataSize"]
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
 - IFsiFileItem.get_DataSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsiFileItem::get_DataSize


## -description


Retrieves the number of bytes in the file.


## -parameters




### -param pVal [out]

Size, in bytes, of the file. 


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




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem">IFsiFileItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem-get_datasize32bithigh">IFsiFileItem::get_DataSize32BitHigh</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem-get_datasize32bitlow">IFsiFileItem::get_DataSize32BitLow</a>
 

 

