---
UID: NS:wabapi._WABIMPORTPARAM
title: WABIMPORTPARAM (wabapi.h)
description: Do not use. Structure passed to Import that gives information about importing .wab files.
helpviewer_keywords: ["*LPWABIMPORTPARAM","LPWABIMPORTPARAM","LPWABIMPORTPARAM structure pointer [Windows Address Book]","MAPI_DIALOG","WABIMPORTPARAM","WABIMPORTPARAM structure [Windows Address Book]","_wab_WABIMPORTPARAM","wab._wab_WABIMPORTPARAM","wabapi/LPWABIMPORTPARAM","wabapi/WABIMPORTPARAM"]
old-location: wab\_wab_WABIMPORTPARAM.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\wabimportparam.htm
ms.date: 12/05/2018
ms.keywords: '*LPWABIMPORTPARAM, LPWABIMPORTPARAM, LPWABIMPORTPARAM structure pointer [Windows Address Book], MAPI_DIALOG, WABIMPORTPARAM, WABIMPORTPARAM structure [Windows Address Book], _wab_WABIMPORTPARAM, wab._wab_WABIMPORTPARAM, wabapi/LPWABIMPORTPARAM, wabapi/WABIMPORTPARAM'
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
req.typenames: WABIMPORTPARAM, *LPWABIMPORTPARAM
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - _WABIMPORTPARAM
 - wabapi/_WABIMPORTPARAM
 - LPWABIMPORTPARAM
 - wabapi/LPWABIMPORTPARAM
 - WABIMPORTPARAM
 - wabapi/WABIMPORTPARAM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabapi.h
api_name:
 - WABIMPORTPARAM
---

# WABIMPORTPARAM structure


## -description

Do not use. Structure passed to <a href="/windows/desktop/api/wabapi/nf-wabapi-iwabobject-import">Import</a> that gives information about importing .wab files.

## -struct-fields

### -field cbSize

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies the size of the structure in bytes.

### -field lpAdrBook

Type: <b><a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a>*</b>

Pointer to an <a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a> interface that specifies the address book object to import to.

### -field hWnd

### -field ulFlags

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies flags affecting behavior.



#### MAPI_DIALOG

Causes <a href="/windows/desktop/api/wabapi/nf-wabapi-iwabobject-import">Import</a> to show a dialog box with a progress bar indicating the progress of the import process.

### -field lpszFileName

Type: <b>LPSTR</b>

Value of type <b>LPSTR</b> that specifies the filename to import, or <b>NULL</b> to cause a FileOpen dialog box to open.

### -field hwnd

Type: <b>HWND</b>

Value of type <b>HWND</b> that specifies the parent window handle for any dialog boxes.