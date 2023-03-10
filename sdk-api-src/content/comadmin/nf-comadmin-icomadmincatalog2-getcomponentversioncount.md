---
UID: NF:comadmin.ICOMAdminCatalog2.GetComponentVersionCount
title: ICOMAdminCatalog2::GetComponentVersionCount (comadmin.h)
description: Retrieves the number of partitions in which a specified component is installed.
helpviewer_keywords: ["GetComponentVersionCount","GetComponentVersionCount method [COM+]","GetComponentVersionCount method [COM+]","ICOMAdminCatalog2 interface","ICOMAdminCatalog2 interface [COM+]","GetComponentVersionCount method","ICOMAdminCatalog2.GetComponentVersionCount","ICOMAdminCatalog2::GetComponentVersionCount","_cos_icomadmincatalog2_GetComponentVersionCount","comadmin/ICOMAdminCatalog2::GetComponentVersionCount","cos.icomadmincatalog2_getcomponentversioncount"]
old-location: cos\icomadmincatalog2_getcomponentversioncount.htm
tech.root: cos
ms.assetid: 5bbae408-3dbe-4f8f-92db-9ea1b8abd9ce
ms.date: 12/05/2018
ms.keywords: GetComponentVersionCount, GetComponentVersionCount method [COM+], GetComponentVersionCount method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],GetComponentVersionCount method, ICOMAdminCatalog2.GetComponentVersionCount, ICOMAdminCatalog2::GetComponentVersionCount, _cos_icomadmincatalog2_GetComponentVersionCount, comadmin/ICOMAdminCatalog2::GetComponentVersionCount, cos.icomadmincatalog2_getcomponentversioncount
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
 - ICOMAdminCatalog2::GetComponentVersionCount
 - comadmin/ICOMAdminCatalog2::GetComponentVersionCount
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
 - ICOMAdminCatalog2.GetComponentVersionCount
---

# ICOMAdminCatalog2::GetComponentVersionCount


## -description

Retrieves the number of partitions in which a specified component is installed.

## -parameters

### -param bstrCLSIDOrProgID [in]

The class ID or program ID of the component.

### -param plVersionCount [out, retval]

The number of different partitions in which the component is installed.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>