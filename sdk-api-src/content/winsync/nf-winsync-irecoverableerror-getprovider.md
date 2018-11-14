---
UID: NF:winsync.IRecoverableError.GetProvider
title: IRecoverableError::GetProvider
author: windows-sdk-content
description: Gets the role of the provider that skipped the item change.
old-location: winsync\irecoverableerror_getprovider.htm
tech.root: winsync
ms.assetid: 48ecfc21-ab30-45c7-879b-c2487288419f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetProvider, GetProvider method [Windows Sync], GetProvider method [Windows Sync],IRecoverableError interface, IRecoverableError interface [Windows Sync],GetProvider method, IRecoverableError.GetProvider, IRecoverableError::GetProvider, winsync.irecoverableerror_getprovider, winsync/IRecoverableError::GetProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - winsync.h
api_name:
 - IRecoverableError.GetProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- winsync.h
: 
- IRecoverableError.GetProvider
: 
---

# IRecoverableError::GetProvider


## -description


Gets the role of the provider that skipped the item change.


## -parameters




### -param pProviderRole [out]

Returns the role of the provider that skipped the item change.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a8b8a84a-6083-4696-bef1-46145a4d71c8">IRecoverableError Interface</a>
 

 

