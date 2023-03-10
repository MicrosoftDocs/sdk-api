---
UID: NN:wuapi.IUpdateCollection
title: IUpdateCollection (wuapi.h)
description: Represents an ordered list of updates.
helpviewer_keywords: ["IUpdateCollection","IUpdateCollection interface [Windows Update Agent]","IUpdateCollection interface [Windows Update Agent]","described","wua.iupdatecollection","wuapi/IUpdateCollection"]
old-location: wua\iupdatecollection.htm
tech.root: wua
ms.assetid: e56a09e9-6a5f-4579-9a5c-987519fccaad
ms.date: 12/05/2018
ms.keywords: IUpdateCollection, IUpdateCollection interface [Windows Update Agent], IUpdateCollection interface [Windows Update Agent],described, wua.iupdatecollection, wuapi/IUpdateCollection
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
 - IUpdateCollection
 - wuapi/IUpdateCollection
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
 - IUpdateCollection
---

# IUpdateCollection interface


## -description

Represents an ordered list of updates.

## -inheritance

The <b>IUpdateCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUpdateCollection</b> also has these types of members:

## -remarks

You can create an instance of this interface by using the UpdateCollection coclass. Use the Microsoft.Update.UpdateColl program identifier to create the object.
