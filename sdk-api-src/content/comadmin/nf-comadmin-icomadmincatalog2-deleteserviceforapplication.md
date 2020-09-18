---
UID: NF:comadmin.ICOMAdminCatalog2.DeleteServiceForApplication
title: ICOMAdminCatalog2::DeleteServiceForApplication (comadmin.h)
description: Deletes the Windows service associated with the specified COM+ application.
helpviewer_keywords: ["DeleteServiceForApplication","DeleteServiceForApplication method [COM+]","DeleteServiceForApplication method [COM+]","ICOMAdminCatalog2 interface","ICOMAdminCatalog2 interface [COM+]","DeleteServiceForApplication method","ICOMAdminCatalog2.DeleteServiceForApplication","ICOMAdminCatalog2::DeleteServiceForApplication","_cos_icomadmincatalog2_DeleteServiceForApplication","comadmin/ICOMAdminCatalog2::DeleteServiceForApplication","cos.icomadmincatalog2_deleteserviceforapplication"]
old-location: cos\icomadmincatalog2_deleteserviceforapplication.htm
tech.root: cos
ms.assetid: 8bc4a72e-79a1-4780-a143-1ba1ec66812b
ms.date: 12/05/2018
ms.keywords: DeleteServiceForApplication, DeleteServiceForApplication method [COM+], DeleteServiceForApplication method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],DeleteServiceForApplication method, ICOMAdminCatalog2.DeleteServiceForApplication, ICOMAdminCatalog2::DeleteServiceForApplication, _cos_icomadmincatalog2_DeleteServiceForApplication, comadmin/ICOMAdminCatalog2::DeleteServiceForApplication, cos.icomadmincatalog2_deleteserviceforapplication
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
 - ICOMAdminCatalog2::DeleteServiceForApplication
 - comadmin/ICOMAdminCatalog2::DeleteServiceForApplication
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
 - ICOMAdminCatalog2.DeleteServiceForApplication
---

# ICOMAdminCatalog2::DeleteServiceForApplication


## -description

Deletes the Windows service associated with the specified COM+ application.

## -parameters

### -param bstrApplicationIDOrName [in]

The application ID or name of the COM+ application to be deleted.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>