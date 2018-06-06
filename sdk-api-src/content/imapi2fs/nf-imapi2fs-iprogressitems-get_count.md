---
UID: NF:imapi2fs.IProgressItems.get_Count
title: IProgressItems::get_Count
author: windows-sdk-content
description: Retrieves the number of progress items in the collection.
old-location: imapi\iprogressitems_get_count.htm
old-project: imapi
ms.assetid: 370386fe-17b0-4cf3-9c28-880a85456e19
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IProgressItems interface [IMAPI],get_Count method, IProgressItems.get_Count, IProgressItems::get_Count, get_Count, get_Count method [IMAPI], get_Count method [IMAPI],IProgressItems interface, imapi.iprogressitems_get_count, imapi2fs/IProgressItems::get_Count
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
 - IProgressItems.get_Count
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IProgressItems::get_Count


## -description


Retrieves the number of progress items in the collection.


## -parameters




### -param Count [out]

Number of progress items in the collection.


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




<a href="https://msdn.microsoft.com/40c28e67-8ff3-4330-90a1-7ebccb0023ad">IProgressItems</a>
 

 

