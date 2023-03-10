---
UID: NN:wuapi.IWindowsDriverUpdateEntry
title: IWindowsDriverUpdateEntry (wuapi.h)
description: Contains the properties that are available only from a Windows driver update.
helpviewer_keywords: ["IWindowsDriverUpdateEntry","IWindowsDriverUpdateEntry interface [Windows Update Agent]","IWindowsDriverUpdateEntry interface [Windows Update Agent]","described","wua.iwindowsdriverupdateentry","wuapi/IWindowsDriverUpdateEntry"]
old-location: wua\iwindowsdriverupdateentry.htm
tech.root: wua
ms.assetid: 91b8ed77-70f7-400f-a887-b3cf9f573c76
ms.date: 12/05/2018
ms.keywords: IWindowsDriverUpdateEntry, IWindowsDriverUpdateEntry interface [Windows Update Agent], IWindowsDriverUpdateEntry interface [Windows Update Agent],described, wua.iwindowsdriverupdateentry, wuapi/IWindowsDriverUpdateEntry
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
 - IWindowsDriverUpdateEntry
 - wuapi/IWindowsDriverUpdateEntry
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
 - IWindowsDriverUpdateEntry
---

# IWindowsDriverUpdateEntry interface


## -description

Contains the properties that are available only from a Windows driver update.

## -remarks

None of the IWindowsDriverUpdateEntry properties are expected to return any errors (other than E_POINTER if <b>NULL</b> is passed to the property).

