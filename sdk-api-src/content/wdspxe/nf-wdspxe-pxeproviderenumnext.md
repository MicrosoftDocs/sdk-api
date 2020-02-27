---
UID: NF:wdspxe.PxeProviderEnumNext
title: PxeProviderEnumNext function (wdspxe.h)
description: Enumerates registered providers.
old-location: wds\pxeproviderenumnext.htm
tech.root: wds
ms.assetid: a76f2d7a-daf4-4258-9c6d-fd0d562f7efe
ms.date: 12/05/2018
ms.keywords: PxeProviderEnumNext, PxeProviderEnumNext function [Windows Deployment Services], wds.pxeproviderenumnext, wdspxe/PxeProviderEnumNext
f1_keywords:
- wdspxe/PxeProviderEnumNext
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- WdsPxe.dll
api_name:
- PxeProviderEnumNext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PxeProviderEnumNext function


## -description


Enumerates registered providers.


## -parameters




### -param hEnum [in]

<b>HANDLE</b> returned by the 
      <a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumfirst">PxeProviderEnumFirst</a> function.


### -param ppProvider [out]

Address of a <a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/ns-wdspxe-pxe_provider">PXE_PROVIDER</a> structure with the 
      <b>uSizeOfStruct</b> member filled in with the size of the structure. On return this 
      structure is filled in with provider information. This structure can be freed with the 
      <a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderfreeinfo">PxeProviderFreeInfo</a> function.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/ns-wdspxe-pxe_provider">PXE_PROVIDER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumclose">PxeProviderEnumClose</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderenumfirst">PxeProviderEnumFirst</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderfreeinfo">PxeProviderFreeInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>
 

 

