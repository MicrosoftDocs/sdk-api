---
UID: NF:wdspxe.PxeProviderEnumFirst
title: PxeProviderEnumFirst function (wdspxe.h)
description: Starts an enumeration of registered providers.
helpviewer_keywords: ["PxeProviderEnumFirst","PxeProviderEnumFirst function [Windows Deployment Services]","wds.pxeproviderenumfirst","wdspxe/PxeProviderEnumFirst"]
old-location: wds\pxeproviderenumfirst.htm
tech.root: wds
ms.assetid: b810455b-219b-49da-a4eb-c1a170711c68
ms.date: 12/05/2018
ms.keywords: PxeProviderEnumFirst, PxeProviderEnumFirst function [Windows Deployment Services], wds.pxeproviderenumfirst, wdspxe/PxeProviderEnumFirst
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
 - PxeProviderEnumFirst
 - wdspxe/PxeProviderEnumFirst
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
 - PxeProviderEnumFirst
---

# PxeProviderEnumFirst function


## -description

Starts an enumeration of registered providers.

## -parameters

### -param phEnum [out]

Address of a <b>HANDLE</b> that on successful return can be used with the 
      <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumnext">PxeProviderEnumNext</a> function to enumerate 
      providers. When the enumeration handle is no longer needed, use the 
      <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumclose">PxeProviderEnumClose</a> function to close the 
      enumeration.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumclose">PxeProviderEnumClose</a>



<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumnext">PxeProviderEnumNext</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>