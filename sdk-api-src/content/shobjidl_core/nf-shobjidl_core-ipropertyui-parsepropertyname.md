---
UID: NF:shobjidl_core.IPropertyUI.ParsePropertyName
title: IPropertyUI::ParsePropertyName
author: windows-sdk-content
description: Developers should use IPropertyDescription instead. Reads the characters of the specified property name and identifies the FMTID and PROPID of the property.
old-location: properties\IPropertyUI_ParsePropertyName.htm
tech.root: properties
ms.assetid: CCD8C646-B259-4445-AEA0-AD7364FE8DEF
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IPropertyUI interface [Windows Properties],ParsePropertyName method, IPropertyUI.ParsePropertyName, IPropertyUI::ParsePropertyName, ParsePropertyName, ParsePropertyName method [Windows Properties], ParsePropertyName method [Windows Properties],IPropertyUI interface, _shell_IPropertyUI_ParsePropertyName, properties.IPropertyUI_ParsePropertyName, shell.IPropertyUI_ParsePropertyName, shobjidl_core/IPropertyUI::ParsePropertyName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPropertyUI.ParsePropertyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyUI::ParsePropertyName


## -description


Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Reads the characters of the specified property name and identifies the FMTID and PROPID of the property.


## -parameters




### -param pszName [in]

Type: <b>LPWSTR</b>

A string specifying the property name to parse.


### -param pfmtid [out]

Type: <b>FMTID*</b>

The FMTID of the parsed property.


### -param ppid [out]

Type: <b>PROPID*</b>

The PROPID of the parsed property name.


### -param pchEaten [in, out]

Type: <b>ULONG*</b>

The number of characters that were consumed in parsing <i>pszName</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



