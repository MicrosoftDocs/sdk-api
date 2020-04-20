---
UID: NF:dwmapi.DwmGetGraphicsStreamClient
title: DwmGetGraphicsStreamClient function (dwmapi.h)
description: This function is not implemented.helpviewer_keywords: ["DwmGetGraphicsStreamClient","DwmGetGraphicsStreamClient function [Desktop Window Manager]","_udwm_dwmgetgraphicsstreamclient","_udwm_dwmgetgraphicsstreamclient_cpp","dwm.dwmgetgraphicsstreamclient","dwmapi/DwmGetGraphicsStreamClient","winui._udwm_dwmgetgraphicsstreamclient"]
old-location: dwm\dwmgetgraphicsstreamclient.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmgetgraphicsstreamclient.htm
ms.date: 12/05/2018
ms.keywords: DwmGetGraphicsStreamClient, DwmGetGraphicsStreamClient function [Desktop Window Manager], _udwm_dwmgetgraphicsstreamclient, _udwm_dwmgetgraphicsstreamclient_cpp, dwm.dwmgetgraphicsstreamclient, dwmapi/DwmGetGraphicsStreamClient, winui._udwm_dwmgetgraphicsstreamclient
f1_keywords:
- dwmapi/DwmGetGraphicsStreamClient
dev_langs:
- c++
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmGetGraphicsStreamClient
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DwmGetGraphicsStreamClient function


## -description


This function is deprecated and only returns DWM_E_COMPOSITIONDISABLED in Windows 7 and later. It may be removed in future versions of Windows.


## -parameters




### -param uIndex


### -param pClientUuid [out]


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



