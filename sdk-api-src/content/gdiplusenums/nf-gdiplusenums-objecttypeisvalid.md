---
UID: NF:gdiplusenums.ObjectTypeIsValid
title: ObjectTypeIsValid function (gdiplusenums.h)
description: The ObjectTypeIsValid function determines whether an element of the ObjectType enumeration represents a valid object type.
helpviewer_keywords: ["ObjectTypeIsValid","ObjectTypeIsValid function [GDI+]","_gdiplus_FUNC_ObjectTypeIsValid_","gdiplus._gdiplus_FUNC_ObjectTypeIsValid_","gdiplusenums/ObjectTypeIsValid"]
old-location: gdiplus\_gdiplus_FUNC_ObjectTypeIsValid_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\objecttypeisvalid.htm
ms.date: 12/05/2018
ms.keywords: ObjectTypeIsValid, ObjectTypeIsValid function [GDI+], _gdiplus_FUNC_ObjectTypeIsValid_, gdiplus._gdiplus_FUNC_ObjectTypeIsValid_, gdiplusenums/ObjectTypeIsValid
req.header: gdiplusenums.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - ObjectTypeIsValid
 - gdiplusenums/ObjectTypeIsValid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - ObjectTypeIsValid
---

# ObjectTypeIsValid function


## -description

The <b>ObjectTypeIsValid</b> function determines whether an element of the ObjectType enumeration represents a valid object type.

## -parameters

### -param type

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-objecttype">ObjectType</a></b>

Element of the ObjectType enumeration to be tested.

## -returns

Type: <b>BOOL</b>

If objectType is equal to ObjectTypeInvalid, this function returns <b>FALSE</b>.

 If objectType is equal to any other element of the ObjectType enumeration, this function returns <b>TRUE</b>.