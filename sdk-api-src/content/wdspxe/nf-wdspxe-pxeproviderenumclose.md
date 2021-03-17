---
UID: NF:wdspxe.PxeProviderEnumClose
title: PxeProviderEnumClose function (wdspxe.h)
description: Closes the enumeration of providers opened by the PxeProviderEnumFirst function.
helpviewer_keywords: ["PxeProviderEnumClose","PxeProviderEnumClose function [Windows Deployment Services]","wds.pxeproviderenumclose","wdspxe/PxeProviderEnumClose"]
old-location: wds\pxeproviderenumclose.htm
tech.root: wds
ms.assetid: 6b71c2cf-a156-4ccb-be7c-2955b4db26a2
ms.date: 12/05/2018
ms.keywords: PxeProviderEnumClose, PxeProviderEnumClose function [Windows Deployment Services], wds.pxeproviderenumclose, wdspxe/PxeProviderEnumClose
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
 - PxeProviderEnumClose
 - wdspxe/PxeProviderEnumClose
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
 - PxeProviderEnumClose
---

# PxeProviderEnumClose function


## -description

Closes the enumeration of providers opened by the 
    <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumfirst">PxeProviderEnumFirst</a> function.

## -parameters

### -param hEnum [in]

<b>HANDLE</b> returned by the 
      <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumfirst">PxeProviderEnumFirst</a> function.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumfirst">PxeProviderEnumFirst</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>