---
UID: NE:wcmconfig.__MIDL___MIDL_itf_wcmconfig_0000_0000_0007
title: WcmNamespaceAccess (wcmconfig.h)
description: Describes the options passed to the ISettingsEngine::GetNamespace method to choose how the namespace must be accessed.
helpviewer_keywords: ["ReadOnlyAccess","ReadWriteAccess","WcmNamespaceAccess","WcmNamespaceAccess enumeration [SMI]","smi.wcmnamespaceaccess","wcmconfig/ReadOnlyAccess","wcmconfig/ReadWriteAccess","wcmconfig/WcmNamespaceAccess"]
old-location: smi\wcmnamespaceaccess.htm
tech.root: SMI
ms.assetid: 11918eab-2f5d-4050-81c6-d4c465b68ce3
ms.date: 12/05/2018
ms.keywords: ReadOnlyAccess, ReadWriteAccess, WcmNamespaceAccess, WcmNamespaceAccess enumeration [SMI], smi.wcmnamespaceaccess, wcmconfig/ReadOnlyAccess, wcmconfig/ReadWriteAccess, wcmconfig/WcmNamespaceAccess
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WcmNamespaceAccess
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wcmconfig_0000_0000_0007
 - wcmconfig/__MIDL___MIDL_itf_wcmconfig_0000_0000_0007
 - WcmNamespaceAccess
 - wcmconfig/WcmNamespaceAccess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WcmConfig.h
api_name:
 - WcmNamespaceAccess
---

# WcmNamespaceAccess enumeration


## -description

Describes the options passed to the <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-getnamespace">ISettingsEngine::GetNamespace</a> method to choose how the namespace must be accessed. Read and write access must be used if the intent is to change settings and read-only access must be used if the intent is only to inspect the settings.

## -enum-fields

### -field ReadOnlyAccess:1

Request read-only access.

### -field ReadWriteAccess:2

Request read and write access.
