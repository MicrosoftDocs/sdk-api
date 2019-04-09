---
UID: NF:comadmin.ICOMAdminCatalog2.CopyComponents
title: ICOMAdminCatalog2::CopyComponents (comadmin.h)
author: windows-sdk-content
description: Copies the specified components from one partition to another.
old-location: cos\icomadmincatalog2_copycomponents.htm
tech.root: cossdk
ms.assetid: 931f4929-b99b-4c4f-8980-eaceacc0e7fa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CopyComponents, CopyComponents method [COM+], CopyComponents method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],CopyComponents method, ICOMAdminCatalog2.CopyComponents, ICOMAdminCatalog2::CopyComponents, _cos_icomadmincatalog2_CopyComponents, comadmin/ICOMAdminCatalog2::CopyComponents, cos.icomadmincatalog2_copycomponents
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
 - ICOMAdminCatalog2.CopyComponents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICOMAdminCatalog2::CopyComponents


## -description


Copies the specified components from one partition to another.


## -parameters




### -param bstrSourceApplicationIDOrName [in]

The application ID or name of the source application.


### -param pVarCLSIDOrProgID [in]

The components to be copied. Each element of the <b>Variant</b> may be a <b>String</b> containing a class ID or program ID, a single catalog object, or a catalog collection (for example, as returned by the <a href="https://msdn.microsoft.com/b1861e8f-bb42-42b5-9435-6fa366f8284a">GetCollectionByQuery2</a> method).


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
<dt><b>COMADMIN_E_AMBIGUOUS_APPLICATION_NAME</b></dt>
</dl>
</td>
<td width="60%">
At least one of the named applications exists in multiple partitions. To avoid this error, use application IDs instead of names.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ffca611d-dacc-47be-9101-9de76ecc8393">ICOMAdminCatalog2</a>
 

 

