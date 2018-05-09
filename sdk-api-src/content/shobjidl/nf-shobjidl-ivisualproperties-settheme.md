---
UID: NF:shobjidl.IVisualProperties.SetTheme
title: IVisualProperties::SetTheme
author: windows-driver-content
description: Sets the specified theme.
old-location: shell\IVisualProperties_SetTheme.htm
old-project: shell
ms.assetid: 0be91bde-ef05-4d64-9f94-91b9020586cb
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IVisualProperties interface [Windows Shell],SetTheme method, IVisualProperties.SetTheme, IVisualProperties::SetTheme, SetTheme, SetTheme method [Windows Shell], SetTheme method [Windows Shell],IVisualProperties interface, _shell_IVisualProperties_SetTheme, shell.IVisualProperties_SetTheme, shobjidl/IVisualProperties::SetTheme
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	IVisualProperties.SetTheme
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IVisualProperties::SetTheme


## -description


Sets the specified theme.


## -parameters




### -param pszSubAppName [in]

Type: <b>LPCWSTR</b>

A pointer to a Unicode string that contains the application name to use in place of the calling application's name. If this parameter is <b>NULL</b>, the calling application's name is used.


### -param pszSubIdList [in]

Type: <b>LPCWSTR</b>

A pointer to a Unicode string that contains a semicolon-separated list of CLSID names for use in place of the actual list passed by the window's class. If this parameter is <b>NULL</b>, the ID list from the calling class is used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



