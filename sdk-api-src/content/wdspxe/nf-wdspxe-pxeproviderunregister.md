---
UID: NF:wdspxe.PxeProviderUnRegister
title: PxeProviderUnRegister function (wdspxe.h)
description: Removes a provider from the list of registered providers.
helpviewer_keywords: ["PxeProviderUnRegister","PxeProviderUnRegister function [Windows Deployment Services]","wds.pxeproviderunregister","wdspxe/PxeProviderUnRegister"]
old-location: wds\pxeproviderunregister.htm
tech.root: wds
ms.assetid: b468d865-c680-4f72-a10c-3d91542df8d3
ms.date: 12/05/2018
ms.keywords: PxeProviderUnRegister, PxeProviderUnRegister function [Windows Deployment Services], wds.pxeproviderunregister, wdspxe/PxeProviderUnRegister
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
 - PxeProviderUnRegister
 - wdspxe/PxeProviderUnRegister
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
 - PxeProviderUnRegister
---

# PxeProviderUnRegister function


## -description

Removes a provider from the list of registered providers.

## -parameters

### -param pszProviderName [in]

Display name for provider from the call to the 
      <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderregister">PxeProviderRegister</a> function.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderregister">PxeProviderRegister</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>