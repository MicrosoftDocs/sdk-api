---
UID: NF:shdeprecated.IBrowserService2._GetToolbarItem
title: IBrowserService2::_GetToolbarItem (shdeprecated.h)
description: Deprecated. Gets a specific item from a toolbar.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_GetToolbarItem method","IBrowserService2._GetToolbarItem","IBrowserService2::_GetToolbarItem","_GetToolbarItem","_GetToolbarItem method [Windows Shell]","_GetToolbarItem method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_GetToolbarItem","shell.IBrowserService2__GetToolbarItem","zone_IBrowserService2__GetToolbarItem"]
old-location: shell\IBrowserService2__GetToolbarItem.htm
tech.root: shell
ms.assetid: 9bce71ca-189e-4072-9acf-10c8b3a34c5c
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_GetToolbarItem method, IBrowserService2._GetToolbarItem, IBrowserService2::_GetToolbarItem, _GetToolbarItem, _GetToolbarItem method [Windows Shell], _GetToolbarItem method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_GetToolbarItem, shell.IBrowserService2__GetToolbarItem, zone_IBrowserService2__GetToolbarItem
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
 - IBrowserService2::_GetToolbarItem
 - shdeprecated/IBrowserService2::_GetToolbarItem
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
 - IBrowserService2._GetToolbarItem
---

# IBrowserService2::_GetToolbarItem


## -description

Deprecated. Gets a specific item from a toolbar.

## -parameters

### -param itb [in]

Type: <b>int</b>

The index of the toolbar item to retrieve.

## -returns

Type: <b>LPTOOLBARITEM</b>

A pointer to a [TOOLBARITEM](./ns-shdeprecated-toolbaritem.md) structure that represents a toolbar item.

## -remarks

This method is implemented by the derived class.