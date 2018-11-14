---
UID: NF:imapi2fs.IFsiNamedStreams.get_EnumNamedStreams
title: IFsiNamedStreams::get_EnumNamedStreams
author: windows-sdk-content
description: Creates a non-variant enumerator for the collection of the named streams associated with a file in the file system image.
old-location: imapi\ifsinamedstreams_get_enumnamedstreams.htm
tech.root: imapi
ms.assetid: 99691d12-bff6-4d75-b9ef-bd92f8198ae2
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IFsiNamedStreams interface [IMAPI],get_EnumNamedStreams method, IFsiNamedStreams.get_EnumNamedStreams, IFsiNamedStreams::get_EnumNamedStreams, get_EnumNamedStreams, get_EnumNamedStreams method [IMAPI], get_EnumNamedStreams method [IMAPI],IFsiNamedStreams interface, imapi.ifsinamedstreams_get_enumnamedstreams, imapi2fs/IFsiNamedStreams::get_EnumNamedStreams
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
 - IFsiNamedStreams.get_EnumNamedStreams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2fs.h
: 
- IFsiNamedStreams.get_EnumNamedStreams
: 
---

# IFsiNamedStreams::get_EnumNamedStreams


## -description


Creates a non-variant enumerator for the collection of the named streams associated with a file in the file system image. 


## -parameters




### -param NewEnum [out, optional]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/f3186af1-4056-4cb5-aac4-5253ee6dbc01">IEnumFsiItems</a> object representing a collection of named streams associated with a file.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
<dt>Value: 0x80004003</dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
<dt>Value: 0x8007000EL</dt>
</dl>
</td>
<td width="60%">
Failed to allocate required memory.

</td>
</tr>
</table>
 




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/383a83e4-5dc2-459a-a58f-b6ce7a656348">IFsiNamedStreams</a>
 

 

