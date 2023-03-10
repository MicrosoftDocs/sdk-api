---
UID: NN:wuapi.IStringCollection
title: IStringCollection (wuapi.h)
description: Represents an ordered list of strings.
helpviewer_keywords: ["IStringCollection","IStringCollection interface [Windows Update Agent]","IStringCollection interface [Windows Update Agent]","described","wua.istringcollection","wuapi/IStringCollection"]
old-location: wua\istringcollection.htm
tech.root: wua
ms.assetid: 3aaab669-1f80-41ee-8c29-6da613ebccff
ms.date: 12/05/2018
ms.keywords: IStringCollection, IStringCollection interface [Windows Update Agent], IStringCollection interface [Windows Update Agent],described, wua.istringcollection, wuapi/IStringCollection
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
 - IStringCollection
 - wuapi/IStringCollection
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
 - IStringCollection
---

# IStringCollection interface


## -description

Represents an ordered list of strings.

## -inheritance

The <b>IStringCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IStringCollection</b> also has these types of members:

## -remarks

This interface can be instantiated by using the StringCollection coclass. Use the Microsoft.Update.StringColl program identifier to create the object.
