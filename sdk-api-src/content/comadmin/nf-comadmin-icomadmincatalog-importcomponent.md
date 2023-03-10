---
UID: NF:comadmin.ICOMAdminCatalog.ImportComponent
title: ICOMAdminCatalog::ImportComponent (comadmin.h)
description: Imports a component already registered as an in-process server into a COM+ application.
helpviewer_keywords: ["ICOMAdminCatalog interface [COM+]","ImportComponent method","ICOMAdminCatalog.ImportComponent","ICOMAdminCatalog::ImportComponent","ImportComponent","ImportComponent method [COM+]","ImportComponent method [COM+]","ICOMAdminCatalog interface","_cos_ICOMAdminCatalog_ImportComponent","comadmin/ICOMAdminCatalog::ImportComponent","cos.icomadmincatalog_importcomponent"]
old-location: cos\icomadmincatalog_importcomponent.htm
tech.root: cos
ms.assetid: 0e29025d-60bc-4f95-a6f9-aa178769855c
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog interface [COM+],ImportComponent method, ICOMAdminCatalog.ImportComponent, ICOMAdminCatalog::ImportComponent, ImportComponent, ImportComponent method [COM+], ImportComponent method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_ImportComponent, comadmin/ICOMAdminCatalog::ImportComponent, cos.icomadmincatalog_importcomponent
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
 - ICOMAdminCatalog::ImportComponent
 - comadmin/ICOMAdminCatalog::ImportComponent
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
 - ICOMAdminCatalog.ImportComponent
---

# ICOMAdminCatalog::ImportComponent


## -description

Imports a component already registered as an in-process server into a COM+ application.

## -parameters

### -param bstrApplIDOrName [in]

The GUID or name of the application.

### -param bstrCLSIDOrProgID [in]

The CLSID or ProgID for the component to import.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

Generally, this method should not be used unless you want to restrict a component to local use only. Otherwise, use the <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog-installcomponent">InstallComponent</a> method instead of <b>ImportComponent</b>. <b>InstallComponent</b> fully registers the component in the COM+ class registration database (RegDB), whereas <b>ImportComponent</b> does not, resulting in an application with limited functionality.

<b>ImportComponent</b> does not bring any interface, method, or type library information for the component into the COM+ class registration database. This behavior restricts how the component can be configured. When you attempt to export a COM+ application that has an imported component to an application proxy, the proxy contains no interface or type library information for the component and marshaling for that component fails.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>