---
UID: NF:comadmin.ICOMAdminCatalog2.GetPartitionName
title: ICOMAdminCatalog2::GetPartitionName method
author: windows-driver-content
description: Retrieves the name of the specified COM+ application.
old-location: cos\icomadmincatalog2_getpartitionname.htm
old-project: cossdk
ms.assetid: 08d3efb2-1e2e-42e3-aefe-644db3b480f4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetPartitionName method [COM+], GetPartitionName method [COM+], ICOMAdminCatalog2 interface, GetPartitionName,ICOMAdminCatalog2.GetPartitionName, ICOMAdminCatalog2, ICOMAdminCatalog2 interface [COM+], GetPartitionName method, ICOMAdminCatalog2::GetPartitionName, _cos_icomadmincatalog2_GetPartitionName, comadmin/ICOMAdminCatalog2::GetPartitionName, cos.icomadmincatalog2_getpartitionname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComAdmin.h
api_name:
-	ICOMAdminCatalog2.GetPartitionName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMAdminCatalog2::GetPartitionName method


## -description


Retrieves  the name of the specified COM+ application.


## -parameters




### -param bstrApplicationIDOrName [in]

The application ID or name of a COM+ application.


### -param pbstrPartitionName [out, retval]

The partition name associated with the specified application.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
<dt><b>COMADMIN_E_AMBIGUOUS_APPLICATION_NAME</b></dt>
</dl>
</td>
<td width="60%">
The named application exists in multiple partitions. To avoid this error, use an application ID instead of a name.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ffca611d-dacc-47be-9101-9de76ecc8393">ICOMAdminCatalog2</a>
 

 

