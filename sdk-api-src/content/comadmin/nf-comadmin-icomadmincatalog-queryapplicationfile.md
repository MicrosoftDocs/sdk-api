---
UID: NF:comadmin.ICOMAdminCatalog.QueryApplicationFile
title: ICOMAdminCatalog::QueryApplicationFile (comadmin.h)
description: Retrieves information about a COM+ application from an application file.
helpviewer_keywords: ["ICOMAdminCatalog interface [COM+]","QueryApplicationFile method","ICOMAdminCatalog.QueryApplicationFile","ICOMAdminCatalog::QueryApplicationFile","QueryApplicationFile","QueryApplicationFile method [COM+]","QueryApplicationFile method [COM+]","ICOMAdminCatalog interface","_cos_ICOMAdminCatalog_QueryApplicationFile","comadmin/ICOMAdminCatalog::QueryApplicationFile","cos.icomadmincatalog_queryapplicationfile"]
old-location: cos\icomadmincatalog_queryapplicationfile.htm
tech.root: cos
ms.assetid: 5f90da9d-06eb-4ec0-8ea1-d040c8e084b7
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog interface [COM+],QueryApplicationFile method, ICOMAdminCatalog.QueryApplicationFile, ICOMAdminCatalog::QueryApplicationFile, QueryApplicationFile, QueryApplicationFile method [COM+], QueryApplicationFile method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_QueryApplicationFile, comadmin/ICOMAdminCatalog::QueryApplicationFile, cos.icomadmincatalog_queryapplicationfile
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ICOMAdminCatalog::QueryApplicationFile
 - comadmin/ICOMAdminCatalog::QueryApplicationFile
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
 - ICOMAdminCatalog.QueryApplicationFile
---

# ICOMAdminCatalog::QueryApplicationFile


## -description

Retrieves information about a COM+ application from an application file.

## -parameters

### -param bstrApplicationFile [in]

The application file from which information is to be retrieved.

### -param pbstrApplicationName [out]

The application name in the specified file.

### -param pbstrApplicationDescription [out]

The application description.

### -param pbHasUsers [out]

Indicates whether the application has user information associated with its roles.

### -param pbIsProxy [out]

Indicates whether the file contains an application proxy.

### -param ppsaVarFileNames [out]

An array of names of the DLL files for the components installed in the application.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>