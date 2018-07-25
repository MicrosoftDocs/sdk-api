---
UID: NF:shobjidl_core.IPropertyUI.GetDefaultWidth
title: IPropertyUI::GetDefaultWidth
author: windows-sdk-content
description: Developers should use IPropertyDescription instead. Gets the width of the property description.
old-location: properties\IPropertyUI_GetDefaultWidth.htm
old-project: properties
ms.assetid: 51A283CF-FA15-478c-B93B-75347308AEEB
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetDefaultWidth, GetDefaultWidth method [Windows Properties], GetDefaultWidth method [Windows Properties],IPropertyUI interface, IPropertyUI interface [Windows Properties],GetDefaultWidth method, IPropertyUI.GetDefaultWidth, IPropertyUI::GetDefaultWidth, _shell_IPropertyUI_GetDefaultWidth, properties.IPropertyUI_GetDefaultWidth, shell.IPropertyUI_GetDefaultWidth, shobjidl_core/IPropertyUI::GetDefaultWidth
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPropertyUI.GetDefaultWidth
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IPropertyUI::GetDefaultWidth


## -description


Developers should use <a href="https://msdn.microsoft.com/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a> instead. Gets the width of the property description.


## -parameters




### -param fmtid [in]

Type: <b>REFFMTID</b>

The FMTID of the property.


### -param pid [in]

Type: <b>PROPID</b>

The PROPID of the property.


### -param pcxChars [out]

Type: <b>ULONG*</b>

The width of the property description.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



