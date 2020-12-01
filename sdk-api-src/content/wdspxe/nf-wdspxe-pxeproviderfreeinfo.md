---
UID: NF:wdspxe.PxeProviderFreeInfo
title: PxeProviderFreeInfo function (wdspxe.h)
description: Frees memory allocated by the PxeProviderEnumNext function.
helpviewer_keywords: ["PxeProviderFreeInfo","PxeProviderFreeInfo function [Windows Deployment Services]","wds.pxeproviderfreeinfo","wdspxe/PxeProviderFreeInfo"]
old-location: wds\pxeproviderfreeinfo.htm
tech.root: wds
ms.assetid: dd0f2b02-afc9-4ff6-b5b8-772ef15e4aa7
ms.date: 12/05/2018
ms.keywords: PxeProviderFreeInfo, PxeProviderFreeInfo function [Windows Deployment Services], wds.pxeproviderfreeinfo, wdspxe/PxeProviderFreeInfo
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
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PxeProviderFreeInfo
 - wdspxe/PxeProviderFreeInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeProviderFreeInfo
---

# PxeProviderFreeInfo function


## -description

Frees memory allocated by the 
    <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumnext">PxeProviderEnumNext</a> function.

## -parameters

### -param pProvider [in]

Address of a <a href="/windows/desktop/api/wdspxe/ns-wdspxe-pxe_provider">PXE_PROVIDER</a> structure returned from the 
      <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumnext">PxeProviderEnumNext</a> function.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -see-also

<a href="/windows/desktop/api/wdspxe/ns-wdspxe-pxe_provider">PXE_PROVIDER</a>



<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumnext">PxeProviderEnumNext</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>