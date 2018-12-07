---
UID: NF:imapi2.IWriteEngine2.get_WriteInProgress
title: IWriteEngine2::get_WriteInProgress
author: windows-sdk-content
description: Retrieves a value that indicates whether the recorder is currently writing data to the disc.
old-location: imapi\iwriteengine2_get_writeinprogress.htm
tech.root: imapi
ms.assetid: 88f67eab-c87b-4a15-b29f-25675d0cac22
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWriteEngine2 interface [IMAPI],get_WriteInProgress method, IWriteEngine2.get_WriteInProgress, IWriteEngine2::get_WriteInProgress, get_WriteInProgress, get_WriteInProgress method [IMAPI], get_WriteInProgress method [IMAPI],IWriteEngine2 interface, imapi.iwriteengine2_get_writeinprogress, imapi2/IWriteEngine2::get_WriteInProgress
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IWriteEngine2.get_WriteInProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWriteEngine2::get_WriteInProgress


## -description


Retrieves a value that indicates whether the recorder is currently writing data to the disc.


## -parameters




### -param value [out]

If VARIANT_TRUE, the recorder is currently writing data to the disc. Otherwise, if VARIANT_FALSE, the recorder is not currently writing to disc.


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




<a href="https://msdn.microsoft.com/89e7526f-2b9b-4f37-b537-5046a0ac283d">IWriteEngine2</a>



<a href="https://msdn.microsoft.com/cd658bd3-71ab-4e63-adec-8b7405a76c12">IWriteEngine2::CancelWrite</a>



<a href="https://msdn.microsoft.com/a6158984-04d3-4919-8a67-fc860b4b3a47">IWriteEngine2::WriteSection</a>
 

 

