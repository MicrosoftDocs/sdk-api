---
UID: NF:oleauto.GetActiveObject
title: GetActiveObject function (oleauto.h)
description: Retrieves a pointer to a running object that has been registered with OLE.
helpviewer_keywords: ["GetActiveObject","GetActiveObject function [Automation]","_oa96_GetActiveObject","automat.getactiveobject","oleauto/GetActiveObject"]
old-location: automat\getactiveobject.htm
tech.root: automat
ms.assetid: a276e30c-6a7f-4cde-9639-21a9f5170b62
ms.date: 12/05/2018
ms.keywords: GetActiveObject, GetActiveObject function [Automation], _oa96_GetActiveObject, automat.getactiveobject, oleauto/GetActiveObject
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetActiveObject
 - oleauto/GetActiveObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - GetActiveObject
---

# GetActiveObject function


## -description

Retrieves a pointer to a running object that has been registered with OLE.

## -parameters

### -param rclsid [in]

The class identifier (CLSID) of the active object from the OLE registration database.

### -param pvReserved

Reserved for future use. Must be null.

### -param ppunk [out]

The requested active object.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

