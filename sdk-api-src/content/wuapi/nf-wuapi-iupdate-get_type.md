---
UID: NF:wuapi.IUpdate.get_Type
title: IUpdate::get_Type (wuapi.h)
description: Gets the type of the update.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","Type property","IUpdate.Type","IUpdate.get_Type","IUpdate::Type","IUpdate::get_Type","Type property [Windows Update Agent]","Type property [Windows Update Agent]","IUpdate interface","get_Type","wua.iupdate_type","wuapi/IUpdate::Type","wuapi/IUpdate::get_Type"]
old-location: wua\iupdate_type.htm
tech.root: wua
ms.assetid: 2556ee19-b6ff-4e66-9e40-2c0a1d6a0176
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],Type property, IUpdate.Type, IUpdate.get_Type, IUpdate::Type, IUpdate::get_Type, Type property [Windows Update Agent], Type property [Windows Update Agent],IUpdate interface, get_Type, wua.iupdate_type, wuapi/IUpdate::Type, wuapi/IUpdate::get_Type
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdate::get_Type
 - wuapi/IUpdate::get_Type
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdate.Type
 - IUpdate.get_Type
---

# IUpdate::get_Type


## -description

Gets the type of the update.

This property is read-only.

## -parameters

### -param retval

A member of the [UpdateType](ne-wuapi-updatetype.md) enumeration specifying the type of the update.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>