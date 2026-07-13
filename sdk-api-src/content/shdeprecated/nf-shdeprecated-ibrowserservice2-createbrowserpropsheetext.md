---
UID: NF:shdeprecated.IBrowserService2.CreateBrowserPropSheetExt
title: IBrowserService2::CreateBrowserPropSheetExt (shdeprecated.h)
description: Deprecated. Allows the derived class to add Folder Options property sheets to the base class.
helpviewer_keywords: ["CreateBrowserPropSheetExt","CreateBrowserPropSheetExt method [Windows Shell]","CreateBrowserPropSheetExt method [Windows Shell]","IBrowserService2 interface","IBrowserService2 interface [Windows Shell]","CreateBrowserPropSheetExt method","IBrowserService2.CreateBrowserPropSheetExt","IBrowserService2::CreateBrowserPropSheetExt","shdeprecated/IBrowserService2::CreateBrowserPropSheetExt","shell.IBrowserService2_CreateBrowserPropSheetExt","zone_IBrowserService2_CreateBrowserPropSheetExt"]
old-location: shell\IBrowserService2_CreateBrowserPropSheetExt.htm
tech.root: shell
ms.assetid: 2738e62b-5577-416b-952e-18a189fc717f
ms.date: 12/05/2018
ms.keywords: CreateBrowserPropSheetExt, CreateBrowserPropSheetExt method [Windows Shell], CreateBrowserPropSheetExt method [Windows Shell],IBrowserService2 interface, IBrowserService2 interface [Windows Shell],CreateBrowserPropSheetExt method, IBrowserService2.CreateBrowserPropSheetExt, IBrowserService2::CreateBrowserPropSheetExt, shdeprecated/IBrowserService2::CreateBrowserPropSheetExt, shell.IBrowserService2_CreateBrowserPropSheetExt, zone_IBrowserService2_CreateBrowserPropSheetExt
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService2::CreateBrowserPropSheetExt
 - shdeprecated/IBrowserService2::CreateBrowserPropSheetExt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2.CreateBrowserPropSheetExt
---

# IBrowserService2::CreateBrowserPropSheetExt


## -description

Deprecated. Allows the derived class to add <b>Folder Options</b> property sheets to the base class.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The IID of the interface pointer that should be returned in the <i>ppv</i> parameter.

### -param ppv [out]

Type: <b>void**</b>

The address of a pointer to the interface pointer requested in the <i>riid</i> parameter.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

