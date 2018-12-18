---
UID: NE:wcmconfig.__MIDL___MIDL_itf_wcmconfig_0000_0000_0007
title: WcmNamespaceAccess
author: windows-sdk-content
description: Describes the options passed to the ISettingsEngine::GetNamespace method to choose how the namespace must be accessed.
old-location: smi\wcmnamespaceaccess.htm
tech.root: SMI
ms.assetid: 11918eab-2f5d-4050-81c6-d4c465b68ce3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ReadOnlyAccess, ReadWriteAccess, WcmNamespaceAccess, WcmNamespaceAccess enumeration [SMI], smi.wcmnamespaceaccess, wcmconfig/ReadOnlyAccess, wcmconfig/ReadWriteAccess, wcmconfig/WcmNamespaceAccess
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WcmConfig.h
api_name:
 - WcmNamespaceAccess
product: Windows
targetos: Windows
req.typenames: WcmNamespaceAccess
req.redist: 
---

# WcmNamespaceAccess enumeration


## -description


Describes the options passed to the <a href="https://msdn.microsoft.com/4f8193f5-9e9f-4819-aa2e-72b8623eca71">ISettingsEngine::GetNamespace</a> method to choose how the namespace must be accessed. Read and write access must be used if the intent is to change settings and read-only access must be used if the intent is only to inspect the settings.


## -enum-fields




### -field ReadOnlyAccess

Request read-only access.


### -field ReadWriteAccess

Request read and write access.

