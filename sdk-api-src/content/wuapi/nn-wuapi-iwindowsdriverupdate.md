---
UID: NN:wuapi.IWindowsDriverUpdate
title: IWindowsDriverUpdate (wuapi.h)
description: Contains the properties and the methods that are available only from a Windows driver update.
helpviewer_keywords: ["IWindowsDriverUpdate","IWindowsDriverUpdate interface [Windows Update Agent]","IWindowsDriverUpdate interface [Windows Update Agent]","described","wua.iwindowsdriverupdate","wuapi/IWindowsDriverUpdate"]
old-location: wua\iwindowsdriverupdate.htm
tech.root: wua
ms.assetid: 4e2eda04-4f86-4919-b754-dba90fa8d5d8
ms.date: 12/05/2018
ms.keywords: IWindowsDriverUpdate, IWindowsDriverUpdate interface [Windows Update Agent], IWindowsDriverUpdate interface [Windows Update Agent],described, wua.iwindowsdriverupdate, wuapi/IWindowsDriverUpdate
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
 - IWindowsDriverUpdate
 - wuapi/IWindowsDriverUpdate
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
 - IWindowsDriverUpdate
---

# IWindowsDriverUpdate interface


## -description

Contains the properties and the methods that are available only from a Windows driver update.

## -remarks

This interface can be obtained by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on an <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a> interface only if the interface represents a Windows driver update.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>