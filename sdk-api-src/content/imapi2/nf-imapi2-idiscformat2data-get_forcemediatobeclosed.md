---
UID: NF:imapi2.IDiscFormat2Data.get_ForceMediaToBeClosed
title: IDiscFormat2Data::get_ForceMediaToBeClosed
author: windows-sdk-content
description: Determines if further additions to the file system are prevented.
old-location: imapi\idiscformat2data_get_forcemediatobeclosed.htm
old-project: imapi
ms.assetid: 9de0afa9-93b7-4a12-b8e2-a9c083692f98
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_ForceMediaToBeClosed method, IDiscFormat2Data.get_ForceMediaToBeClosed, IDiscFormat2Data::get_ForceMediaToBeClosed, get_ForceMediaToBeClosed, get_ForceMediaToBeClosed method [IMAPI], get_ForceMediaToBeClosed method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_forcemediatobeclosed, imapi2/IDiscFormat2Data::get_ForceMediaToBeClosed
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi2.h
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
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2Data.get_ForceMediaToBeClosed
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2Data::get_ForceMediaToBeClosed


## -description


Determines if further additions to the file system are prevented.


## -parameters




### -param value [out]

Is VARIANT_TRUE if the next write session ends by marking the disc as closed to subsequent write sessions. Otherwise, VARIANT_FALSE to keep the disc open for subsequent write sessions. 


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




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/9a087a73-1b61-481d-8deb-a251511906a9">IDiscFormat2Data::put_ForceMediaToBeClosed</a>
 

 

