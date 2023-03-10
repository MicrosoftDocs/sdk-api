---
UID: NC:wabapi.WABOpen
title: WABOpen (wabapi.h)
description: Do not use. Provides access to the address book through a number of object interfaces. The root interface is IAddrBook, which is a subset of the MAPI implementation of IAddrBook.
helpviewer_keywords: ["WABOpen","WABOpen callback","WABOpen callback function [Windows Address Book]","_wab_WABOpen","wab._wab_WABOpen","wabapi/WABOpen"]
old-location: wab\_wab_WABOpen.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\functions\wabopen.htm
ms.date: 12/05/2018
ms.keywords: WABOpen, WABOpen callback, WABOpen callback function [Windows Address Book], _wab_WABOpen, wab._wab_WABOpen, wabapi/WABOpen
req.header: wabapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.5
ms.custom: 19H1
f1_keywords:
 - WABOpen
 - wabapi/WABOpen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wabapi.h
api_name:
 - WABOpen
---

# WABOpen callback function


## -description

Do not use. Provides access to the address book through a number of object interfaces. The root interface is <a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a>, which is a subset of the MAPI implementation of <a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a>.

## -parameters

### -param lppAdrBook

Type: <b>LPADRBOOK*</b>

Address of a pointer to the <a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a> interface returned by the function.

### -param lppWABObject

Type: <b>LPWABOBJECT*</b>

Address of a pointer to the <a href="/windows/desktop/api/wabapi/nn-wabapi-iwabobject">IWABObject</a> interface returned by the function.

### -param lpWP

### -param Reserved2

Type: <b>DWORD</b>

Reserved. Must be set to 0.


#### - lpWABParam

Type: <b>LPWAB_PARAM</b>

Pointer to a <a href="/windows/desktop/api/wabapi/ns-wabapi-wab_param">WAB_PARAM</a> structure. Supported by Internet Explorer 4.0 or later.

## -returns

Type: <b>HRESULT</b>

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/wabapi/nc-wabapi-wabopenex">WABOpenEx</a>