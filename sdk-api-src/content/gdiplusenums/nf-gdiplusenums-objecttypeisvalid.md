---
UID: NF:gdiplusenums.ObjectTypeIsValid
title: ObjectTypeIsValid function
author: windows-sdk-content
description: The ObjectTypeIsValid function determines whether an element of the ObjectType enumeration represents a valid object type.
old-location: gdiplus\_gdiplus_FUNC_ObjectTypeIsValid_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\objecttypeisvalid.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ObjectTypeIsValid, ObjectTypeIsValid function [GDI+], _gdiplus_FUNC_ObjectTypeIsValid_, gdiplus._gdiplus_FUNC_ObjectTypeIsValid_, gdiplusenums/ObjectTypeIsValid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ObjectTypeIsValid function


## -description


The <b>ObjectTypeIsValid</b> function determines whether an element of the ObjectType enumeration represents a valid object type.


## -parameters




### -param type

Type: <b><a href="https://msdn.microsoft.com/9b35cac6-62e7-4ca2-98e2-2a983da565c1">ObjectType</a></b>

Element of the ObjectType enumeration to be tested.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If objectType is equal to ObjectTypeInvalid, this function returns <b>FALSE</b>.

 If objectType is equal to any other element of the ObjectType enumeration, this function returns <b>TRUE</b>.



