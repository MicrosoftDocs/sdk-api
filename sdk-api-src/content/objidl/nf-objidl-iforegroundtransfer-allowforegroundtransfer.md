---
UID: NF:objidl.IForegroundTransfer.AllowForegroundTransfer
title: IForegroundTransfer::AllowForegroundTransfer
author: windows-sdk-content
description: Yields the foreground window to the COM server process.
old-location: com\iforegroundtransfer_allowforegroundtransfer.htm
tech.root: com
ms.assetid: 54d138f5-5f16-4eb8-bbac-2d057b7dab2f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: AllowForegroundTransfer, AllowForegroundTransfer method [COM], AllowForegroundTransfer method [COM],IForegroundTransfer interface, IForegroundTransfer interface [COM],AllowForegroundTransfer method, IForegroundTransfer.AllowForegroundTransfer, IForegroundTransfer::AllowForegroundTransfer, _com_iforegroundtransfer_allowforegroundtransfer, com.iforegroundtransfer_allowforegroundtransfer, objidl/IForegroundTransfer::AllowForegroundTransfer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - ObjIdl.h
api_name:
 - IForegroundTransfer.AllowForegroundTransfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IForegroundTransfer::AllowForegroundTransfer


## -description


Yields the foreground window to the COM server process.


## -parameters




### -param lpvReserved [in]

This parameter is reserved and must be <b>NULL</b>.


## -returns



This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvReserved</i> parameter is not <b>NULL</b>, or this interface is on a proxy that does not support foreground control.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a728aaad-3d7a-425c-b886-ba35c4fa54d0">CoAllowSetForegroundWindow</a>



<a href="https://msdn.microsoft.com/21857592-0f98-4eb4-a153-4ce20edf26c7">IForegroundTransfer</a>
 

 

