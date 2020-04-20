---
UID: NF:imapi2fs.IFsiNamedStreams.get_Count
title: IFsiNamedStreams::get_Count (imapi2fs.h)
description: Returns the number of the named streams associated with a file in the file system image.helpviewer_keywords: ["IFsiNamedStreams interface [IMAPI]","get_Count method","IFsiNamedStreams.get_Count","IFsiNamedStreams::get_Count","get_Count","get_Count method [IMAPI]","get_Count method [IMAPI]","IFsiNamedStreams interface","imapi.ifsinamedstreams_get_count","imapi2fs/IFsiNamedStreams::get_Count"]
old-location: imapi\ifsinamedstreams_get_count.htm
tech.root: imapi
ms.assetid: 3d4efee2-607b-4be4-9854-79fed47503e4
ms.date: 12/05/2018
ms.keywords: IFsiNamedStreams interface [IMAPI],get_Count method, IFsiNamedStreams.get_Count, IFsiNamedStreams::get_Count, get_Count, get_Count method [IMAPI], get_Count method [IMAPI],IFsiNamedStreams interface, imapi.ifsinamedstreams_get_count, imapi2fs/IFsiNamedStreams::get_Count
f1_keywords:
- imapi2fs/IFsiNamedStreams.get_Count
dev_langs:
- c++
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
- IFsiNamedStreams.get_Count
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsiNamedStreams::get_Count


## -description


Returns the number of the named streams associated with a file in the file system image.


## -parameters




### -param count [out]

Pointer to a value indicating the total number of named streams in the collection.


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
</table>
 




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams">IFsiNamedStreams</a>
 

 

