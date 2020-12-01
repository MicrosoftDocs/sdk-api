---
UID: NS:wdspxe.tagPXE_PROVIDER
title: PXE_PROVIDER (wdspxe.h)
description: Describes a provider.
helpviewer_keywords: ["*PPXE_PROVIDER","PPXE_PROVIDER","PPXE_PROVIDER structure pointer [Windows Deployment Services]","PXE_PROVIDER","PXE_PROVIDER structure [Windows Deployment Services]","wds.pxe_provider","wdspxe/PPXE_PROVIDER","wdspxe/PXE_PROVIDER"]
old-location: wds\pxe_provider.htm
tech.root: wds
ms.assetid: a07afefd-7a97-42bb-8d70-2bc7c51ddef3
ms.date: 12/05/2018
ms.keywords: '*PPXE_PROVIDER, PPXE_PROVIDER, PPXE_PROVIDER structure pointer [Windows Deployment Services], PXE_PROVIDER, PXE_PROVIDER structure [Windows Deployment Services], wds.pxe_provider, wdspxe/PPXE_PROVIDER, wdspxe/PXE_PROVIDER'
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PXE_PROVIDER, *PPXE_PROVIDER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPXE_PROVIDER
 - wdspxe/tagPXE_PROVIDER
 - PPXE_PROVIDER
 - wdspxe/PPXE_PROVIDER
 - PXE_PROVIDER
 - wdspxe/PXE_PROVIDER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WdsPxe.h
api_name:
 - PXE_PROVIDER
---

# PXE_PROVIDER structure


## -description

Describes a provider.

## -struct-fields

### -field uSizeOfStruct

Size of the <b>PXE_PROVIDER</b> structure.

### -field pwszName

Address of a null-terminated string that specifies the display name of the provider. This name is displayed 
      to the user and must be unique among registered providers.

### -field pwszFilePath

Address of a null-terminated string that specifies the full path to the provider DLL.

### -field bIsCritical

Indicates whether the provider is critical. If a critical provider fails, the WDS server will also 
      fail.

### -field uIndex

Index of a provider in the list of registered providers.

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumnext">PxeProviderEnumNext</a>



<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderfreeinfo">PxeProviderFreeInfo</a>



<a href="/windows/desktop/Wds/windows-deployment-services-structures">Windows Deployment Services Structures</a>