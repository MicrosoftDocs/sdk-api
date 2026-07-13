---
UID: NF:uiautomationcore.ICustomNavigationProvider.Navigate
tech.root: WinAuto
title: ICustomNavigationProvider::Navigate
ms.date: 01/07/2026
targetos: Windows
description: Moves to the next element in the specified direction within the logical UI tree.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: uiautomationcore.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows build 26100
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - uiautomationcore.h
api_name:
 - ICustomNavigationProvider::Navigate
f1_keywords:
 - ICustomNavigationProvider::Navigate
 - uiautomationcore/ICustomNavigationProvider::Navigate
dev_langs:
 - c++
helpviewer_keywords:
 - Navigate
---

# Navigate function

## -description

Moves to the next element in the specified direction within the logical UI tree.

## -parameters

### -param direction [in]

The specified direction.

### -param pRetVal [out, retval]

Pointer to the [IRawElementProviderSimple](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple) interface that was retrieved as a property.

## -returns

Type: **[HRESULT](/windows/desktop/WinProg/windows-data-types)**

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

## -see-also
