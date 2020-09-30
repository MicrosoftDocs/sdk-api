---
UID: NF:comadmin.ICOMAdminCatalog2.CopyApplications
title: ICOMAdminCatalog2::CopyApplications (comadmin.h)
description: Copies the specified COM+ applications from one partition to another.
helpviewer_keywords: ["CopyApplications","CopyApplications method [COM+]","CopyApplications method [COM+]","ICOMAdminCatalog2 interface","ICOMAdminCatalog2 interface [COM+]","CopyApplications method","ICOMAdminCatalog2.CopyApplications","ICOMAdminCatalog2::CopyApplications","_cos_icomadmincatalog2_CopyApplications","comadmin/ICOMAdminCatalog2::CopyApplications","cos.icomadmincatalog2_copyapplications"]
old-location: cos\icomadmincatalog2_copyapplications.htm
tech.root: cos
ms.assetid: 4ddb9cab-2e02-4b96-9216-d6cb064f8107
ms.date: 12/05/2018
ms.keywords: CopyApplications, CopyApplications method [COM+], CopyApplications method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],CopyApplications method, ICOMAdminCatalog2.CopyApplications, ICOMAdminCatalog2::CopyApplications, _cos_icomadmincatalog2_CopyApplications, comadmin/ICOMAdminCatalog2::CopyApplications, cos.icomadmincatalog2_copyapplications
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICOMAdminCatalog2::CopyApplications
 - comadmin/ICOMAdminCatalog2::CopyApplications
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2.CopyApplications
---

# ICOMAdminCatalog2::CopyApplications


## -description

Copies the specified COM+ applications from one partition to another.

## -parameters

### -param bstrSourcePartitionIDOrName [in]

The partition GUID or the name of the source partition.

### -param pVarApplicationID [in]

The applications to be copied. Each element of the <b>Variant</b> may be a <b>String</b> containing an application name or ID, a single catalog object, or a catalog collection (as returned, for example, by the <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getcollectionbyquery2">GetCollectionByQuery2</a> method).

### -param bstrDestinationPartitionIDOrName [in]

The partition GUID or the name of the destination partition.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>