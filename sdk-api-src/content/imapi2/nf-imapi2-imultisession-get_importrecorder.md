---
UID: NF:imapi2.IMultisession.get_ImportRecorder
title: IMultisession::get_ImportRecorder
author: windows-sdk-content
description: Retrieves the disc recorder to use to import one or more previous sessions.
old-location: imapi\imultisession_get_importrecorder.htm
tech.root: imapi
ms.assetid: eca127eb-0e0a-4f43-afa4-42fde8d43284
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IMultisession interface [IMAPI],get_ImportRecorder method, IMultisession.get_ImportRecorder, IMultisession::get_ImportRecorder, get_ImportRecorder, get_ImportRecorder method [IMAPI], get_ImportRecorder method [IMAPI],IMultisession interface, imapi.imultisession_get_importrecorder, imapi2/IMultisession::get_ImportRecorder
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
 - IMultisession.get_ImportRecorder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMultisession::get_ImportRecorder


## -description


Retrieves the disc recorder to use to import one or more previous sessions.


## -parameters




### -param value [out]

An <a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a> interface that identifies the device that contains one or more session images to import.


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



The import recorder reads session content from the optical media and provides it to <a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>.




## -see-also




<a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a>
 

 

