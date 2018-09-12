---
UID: NF:comadmin.ICOMAdminCatalog2.ShutdownApplicationInstances
title: ICOMAdminCatalog2::ShutdownApplicationInstances
author: windows-sdk-content
description: Initiates shutdown of the specified application server processes.
old-location: cos\icomadmincatalog2_shutdownapplicationinstances.htm
tech.root: cossdk
ms.assetid: 1de6c76b-f6f1-44d3-9bd4-4b6ac921893a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICOMAdminCatalog2 interface [COM+],ShutdownApplicationInstances method, ICOMAdminCatalog2.ShutdownApplicationInstances, ICOMAdminCatalog2::ShutdownApplicationInstances, ShutdownApplicationInstances, ShutdownApplicationInstances method [COM+], ShutdownApplicationInstances method [COM+],ICOMAdminCatalog2 interface, _cos_icomadmincatalog2_ShutdownApplicationInstances, comadmin/ICOMAdminCatalog2::ShutdownApplicationInstances, cos.icomadmincatalog2_shutdownapplicationinstances
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2.ShutdownApplicationInstances
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICOMAdminCatalog2::ShutdownApplicationInstances


## -description


Initiates shutdown of the specified application server processes.


## -parameters




### -param pVarApplicationInstanceID [in]

The application instances to be shut down. Each element of the <b>Variant</b> may be a <b>String</b> containing an application instance GUID (for example, as returned by the <a href="https://msdn.microsoft.com/en-us/library/ms685077(v=VS.85).aspx">GetApplicationInstanceIDFromProcessID</a> method), a single catalog object, or a catalog collection (for example, as returned by the <a href="https://msdn.microsoft.com/en-us/library/ms685970(v=VS.85).aspx">GetCollectionByQuery2</a> method).


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
<dt><b>COMADIN_E_OBJECT_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
A specified application instance does not exist.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee309562(v=VS.85).aspx">ICOMAdminCatalog2</a>
 

 

