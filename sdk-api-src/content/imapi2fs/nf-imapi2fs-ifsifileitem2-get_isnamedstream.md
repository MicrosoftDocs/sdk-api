---
UID: NF:imapi2fs.IFsiFileItem2.get_IsNamedStream
title: IFsiFileItem2::get_IsNamedStream (imapi2fs.h)
author: windows-sdk-content
description: Determines if the item is a named stream.
old-location: imapi\ifsifileitem2_get_isnamedstream.htm
tech.root: imapi
ms.assetid: 56e89b63-6fb5-4509-b90f-f25ec0cf2bd2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsiFileItem2 interface [IMAPI],get_IsNamedStream method, IFsiFileItem2.get_IsNamedStream, IFsiFileItem2::get_IsNamedStream, get_IsNamedStream, get_IsNamedStream method [IMAPI], get_IsNamedStream method [IMAPI],IFsiFileItem2 interface, imapi.ifsifileitem2_get_isnamedstream, imapi2fs/IFsiFileItem2::get_IsNamedStream
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
req.idl: Imapi2.idl
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
 - IFsiFileItem2.get_IsNamedStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsiFileItem2::get_IsNamedStream


## -description


Determines if the item is a named stream. Data streams for named streams contained within the file system image are read-only. Stream data can only be replaced by overwriting the existing named stream.


## -parameters




### -param pVal [out]

Pointer to a value that indicates if the item is a named stream. to <b>VARIANT_TRUE</b> if an ; otherwise, <b>VARIANT_FALSE</b>.


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



The user must enable UDF and set the UDF revision to 2.00 or higher to support named streams.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/f35d1cd9-8a04-4c12-9af3-38f2c44b8c06">IFsiFileItem2</a>
 

 

