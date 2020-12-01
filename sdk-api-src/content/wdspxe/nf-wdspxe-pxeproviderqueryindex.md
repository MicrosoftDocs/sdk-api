---
UID: NF:wdspxe.PxeProviderQueryIndex
title: PxeProviderQueryIndex function (wdspxe.h)
description: Returns the index of the specified provider in the list of registered providers.
helpviewer_keywords: ["PxeProviderQueryIndex","PxeProviderQueryIndex function [Windows Deployment Services]","wds.pxeproviderqueryindex","wdspxe/PxeProviderQueryIndex"]
old-location: wds\pxeproviderqueryindex.htm
tech.root: wds
ms.assetid: 0b28c075-7f2e-4149-b851-21614773e942
ms.date: 12/05/2018
ms.keywords: PxeProviderQueryIndex, PxeProviderQueryIndex function [Windows Deployment Services], wds.pxeproviderqueryindex, wdspxe/PxeProviderQueryIndex
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
 - PxeProviderQueryIndex
 - wdspxe/PxeProviderQueryIndex
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
 - PxeProviderQueryIndex
---

# PxeProviderQueryIndex function


## -description

Returns the index of the specified provider in the list of registered providers.

## -parameters

### -param pszProviderName [in]

Friendly name for the provider from the call to the 
      <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderregister">PxeProviderRegister</a> function.

### -param puIndex [out]

Address of a <b>ULONG</b> that will receive the index of the provider.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -remarks

If a provider wants to insert itself in the list of registered providers in a specific order (that is, wants to 
    service client requests before or after a certain provider), it can query the index of another provider and then use 
    the returned index to decide its own location.


#### Examples


```cpp
//
// Suppose Provider wants to handle requests after BINLSVC has rejected them.
//
dwError = PxeProviderQueryIndex(L"BINLSVC", &Index);

if (dwError == ERROR_SUCCESS)
{
 if (PxeProviderRegister(L"MYPROV",
                         L"C:\\MyDir\\MyProv.DLL",
                         PXE_REG_INDEX_BOTTOM,
                         Index + 1,              // Add after BINLSVC
                         &hKey) != ERROR_SUCCESS)
 {
  // Handle Error
 }
}

```

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxeproviderregister">PxeProviderRegister</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>