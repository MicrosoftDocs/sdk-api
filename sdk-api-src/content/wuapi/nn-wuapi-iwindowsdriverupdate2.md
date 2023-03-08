---
UID: NN:wuapi.IWindowsDriverUpdate2
title: IWindowsDriverUpdate2 (wuapi.h)
description: Contains the properties and methods that are available only from a Windows driver update. (IWindowsDriverUpdate2)
helpviewer_keywords: ["IWindowsDriverUpdate2","IWindowsDriverUpdate2 interface [Windows Update Agent]","IWindowsDriverUpdate2 interface [Windows Update Agent]","described","wua.iwindowsdriverupdate2","wuapi/IWindowsDriverUpdate2"]
old-location: wua\iwindowsdriverupdate2.htm
tech.root: wua
ms.assetid: 9a2d6318-c5f0-41bc-a4df-bb9a53c9dee4
ms.date: 12/05/2018
ms.keywords: IWindowsDriverUpdate2, IWindowsDriverUpdate2 interface [Windows Update Agent], IWindowsDriverUpdate2 interface [Windows Update Agent],described, wua.iwindowsdriverupdate2, wuapi/IWindowsDriverUpdate2
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
 - IWindowsDriverUpdate2
 - wuapi/IWindowsDriverUpdate2
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
 - IWindowsDriverUpdate2
---

# IWindowsDriverUpdate2 interface


## -description

Contains the properties and methods that are available only from a Windows driver update.

## -inheritance

The <b>IWindowsDriverUpdate2</b> interface inherits from <a href="/windows/desktop/api/wuapi/nn-wuapi-iwindowsdriverupdate">IWindowsDriverUpdate</a>. <b>IWindowsDriverUpdate2</b> also has these types of members:

## -remarks

This interface can be obtained by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on an <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a> interface only if the interface represents a Windows Driver update.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iwindowsdriverupdate">IWindowsDriverUpdate</a>
