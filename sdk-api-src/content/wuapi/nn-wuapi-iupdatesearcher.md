---
UID: NN:wuapi.IUpdateSearcher
title: IUpdateSearcher (wuapi.h)
description: Searches for updates on a server. (IUpdateSearcher)
helpviewer_keywords: ["IUpdateSearcher","IUpdateSearcher interface [Windows Update Agent]","IUpdateSearcher interface [Windows Update Agent]","described","wua.iupdatesearcher","wuapi/IUpdateSearcher"]
old-location: wua\iupdatesearcher.htm
tech.root: wua
ms.assetid: f41b1689-d9fe-4697-91e9-a176d3b592c7
ms.date: 12/05/2018
ms.keywords: IUpdateSearcher, IUpdateSearcher interface [Windows Update Agent], IUpdateSearcher interface [Windows Update Agent],described, wua.iupdatesearcher, wuapi/IUpdateSearcher
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
 - IUpdateSearcher
 - wuapi/IUpdateSearcher
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
 - IUpdateSearcher
---

# IUpdateSearcher interface


## -description

Searches for updates on a server.

## -inheritance

The <b>IUpdateSearcher</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUpdateSearcher</b> also has these types of members:

## -remarks

You can create an instance of this interface by using the UpdateSearcher coclass. Use the Microsoft.Update.Searcher program identifier to create the object.
