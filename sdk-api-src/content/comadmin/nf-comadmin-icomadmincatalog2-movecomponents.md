---
UID: NF:comadmin.ICOMAdminCatalog2.MoveComponents
title: ICOMAdminCatalog2::MoveComponents
author: windows-sdk-content
description: Moves the specified components from one application to another.
old-location: cos\icomadmincatalog2_movecomponents.htm
old-project: cossdk
ms.assetid: 38cc4726-4b61-4f4b-9719-161297361f45
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ICOMAdminCatalog2 interface [COM+],MoveComponents method, ICOMAdminCatalog2.MoveComponents, ICOMAdminCatalog2::MoveComponents, MoveComponents, MoveComponents method [COM+], MoveComponents method [COM+],ICOMAdminCatalog2 interface, _cos_icomadmincatalog2_MoveComponents, comadmin/ICOMAdminCatalog2::MoveComponents, cos.icomadmincatalog2_movecomponents
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2.MoveComponents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMAdminCatalog2::MoveComponents


## -description


Moves the specified components from one application to another.


## -parameters




### -param bstrSourceApplicationIDOrName [in]

The application ID or name of the source application.


### -param pVarCLSIDOrProgID [in]

The components to be moved. Each element of the <b>Variant</b> may be a <b>String</b> containing a class ID or program ID, a single catalog object, or a catalog collection (for example, as returned by the <a href="https://msdn.microsoft.com/b1861e8f-bb42-42b5-9435-6fa366f8284a">GetCollectionByQuery2</a> method).


### -param bstrDestinationApplicationIDOrName [in]

The application ID or name of the destination application.


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
<dt><b>COMADIN_E_AMBIGUOUS_APPLICATION_NAME</b></dt>
</dl>
</td>
<td width="60%">
At least one of the named applications exists in multiple partitions. To avoid this error, use application IDs instead of names.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ffca611d-dacc-47be-9101-9de76ecc8393">ICOMAdminCatalog2</a>
 

 

