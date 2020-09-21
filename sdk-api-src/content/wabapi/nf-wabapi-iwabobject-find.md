---
UID: NF:wabapi.IWABObject.Find
title: IWABObject::Find (wabapi.h)
description: Launches the Windows Address Book (WAB) Find dialog box.
helpviewer_keywords: ["Find","Find method [Windows Address Book]","Find method [Windows Address Book]","IWABObject interface","IWABObject interface [Windows Address Book]","Find method","IWABObject.Find","IWABObject::Find","_wab_IWABObject_Find","wab._wab_IWABObject_Find","wabapi/IWABObject::Find"]
old-location: wab\_wab_IWABObject_Find.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\find.htm
ms.date: 12/05/2018
ms.keywords: Find, Find method [Windows Address Book], Find method [Windows Address Book],IWABObject interface, IWABObject interface [Windows Address Book],Find method, IWABObject.Find, IWABObject::Find, _wab_IWABObject_Find, wab._wab_IWABObject_Find, wabapi/IWABObject::Find
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
req.dll: Wab32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5
ms.custom: 19H1
f1_keywords:
 - IWABObject::Find
 - wabapi/IWABObject::Find
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IWABObject.Find
---

# IWABObject::Find


## -description

Launches the Windows Address Book (WAB) Find dialog box.

## -parameters

### -param lpIAB

Type: <b><a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a>*</b>

Pointer to an <a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a> interface 
				that specifies the address book to search.

### -param hWnd

Type: <b>HWND</b>

Value of type <b>HWND</b> that specifies 
				the handle to the parent window for the Find dialog box. 
				The value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful.