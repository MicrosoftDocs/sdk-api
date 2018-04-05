---
UID: NF:imapi2fs.IFsiItem.get_IsHidden
title: IFsiItem::get_IsHidden method
author: windows-driver-content
description: Determines if the item's hidden attribute is set in the file system image.
old-location: imapi\ifsiitem_get_ishidden.htm
old-project: imapi
ms.assetid: 1aec5bbc-d602-40c1-80e4-cad9dd8a2ab5
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IFsiItem, IFsiItem interface [IMAPI], get_IsHidden method, IFsiItem::get_IsHidden, get_IsHidden method [IMAPI], get_IsHidden method [IMAPI], IFsiItem interface, get_IsHidden,IFsiItem.get_IsHidden, imapi.ifsiitem_get_ishidden, imapi2fs/IFsiItem::get_IsHidden
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
-	IFsiItem.get_IsHidden
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFsiItem::get_IsHidden method


## -description


Determines if the item's hidden attribute is set in the file system image. 


## -parameters




### -param pVal [out]

Is VARIANT_TRUE if the hidden attribute of the item is marked in the file system image; otherwise, VARIANT_FALSE.


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




<a href="https://msdn.microsoft.com/44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0">IFsiItem</a>



<a href="https://msdn.microsoft.com/a437daea-af30-43e5-bb88-e59de8ba37c9">IFsiItem::put_IsHidden</a>
 

 

