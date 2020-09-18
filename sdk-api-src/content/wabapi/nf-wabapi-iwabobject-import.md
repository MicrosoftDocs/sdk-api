---
UID: NF:wabapi.IWABObject.Import
title: IWABObject::Import (wabapi.h)
description: Imports a .wab file into the user's Address Book.
helpviewer_keywords: ["IWABObject interface [Windows Address Book]","Import method","IWABObject.Import","IWABObject::Import","Import","Import method [Windows Address Book]","Import method [Windows Address Book]","IWABObject interface","_wab_IWABObject_Import","wab._wab_IWABObject_Import","wabapi/IWABObject::Import"]
old-location: wab\_wab_IWABObject_Import.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\import.htm
ms.date: 12/05/2018
ms.keywords: IWABObject interface [Windows Address Book],Import method, IWABObject.Import, IWABObject::Import, Import, Import method [Windows Address Book], Import method [Windows Address Book],IWABObject interface, _wab_IWABObject_Import, wab._wab_IWABObject_Import, wabapi/IWABObject::Import
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
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IWABObject::Import
 - wabapi/IWABObject::Import
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
 - IWABObject.Import
---

# IWABObject::Import


## -description

Imports a .wab file into the user's Address Book.

## -parameters

### -param lpWIP

Type: <b>LPSTR</b>

Pointer to a <a href="/windows/desktop/api/wabapi/ns-wabapi-wabimportparam">WABIMPORTPARAM</a> 
				structure.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.

## -remarks

When calling this method, pass a pointer to a 
	<a href="/windows/desktop/api/wabapi/ns-wabapi-wabimportparam">WABIMPORTPARAM</a> structure. If the caller specifies 
	<b>MAPI_DIALOG</b> in the 
	<b>ulFlags</b> member of the structure, 
	the Windows Address Book (WAB) shows a dialog box with a progress bar indicating 
	the progress of the import process. The caller can specify a file name 
	to import. If the caller specifies a <b>NULL</b> file name, the 
	WAB opens a <a href="/windows/desktop/api/commdlg/nf-commdlg-getopenfilenamea">GetOpenFileName</a> 
	dialog box to prompt the user to select a .wab file for importing.

For compatibility with previously released versions of the 
	WAB that expose this method, the pointer to the 
	<a href="/windows/desktop/api/wabapi/ns-wabapi-wabimportparam">WABIMPORTPARAM</a> structure needs to be cast to an 
	<b>LPSTR</b> prior to passing it into this method.