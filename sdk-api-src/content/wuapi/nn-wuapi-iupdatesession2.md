---
UID: NN:wuapi.IUpdateSession2
title: IUpdateSession2 (wuapi.h)
description: Represents a session in which the caller can perform operations that involve updates. For example, this interface represents sessions in which the caller performs a search, download, installation, or uninstallation operation. (IUpdateSession2)
helpviewer_keywords: ["IUpdateSession2","IUpdateSession2 interface [Windows Update Agent]","IUpdateSession2 interface [Windows Update Agent]","described","wua.iupdatesession2","wuapi/IUpdateSession2"]
old-location: wua\iupdatesession2.htm
tech.root: wua
ms.assetid: c074cbc8-6d1b-41dd-a54c-30f02fca9215
ms.date: 12/05/2018
ms.keywords: IUpdateSession2, IUpdateSession2 interface [Windows Update Agent], IUpdateSession2 interface [Windows Update Agent],described, wua.iupdatesession2, wuapi/IUpdateSession2
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
 - IUpdateSession2
 - wuapi/IUpdateSession2
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
 - IUpdateSession2
---

# IUpdateSession2 interface


## -description

Represents a session in which the caller can perform operations that involve updates. For example, this interface represents sessions in which the caller performs a search, download, installation, or uninstallation operation.

## -remarks

You can create an instance of this interface by using the UpdateSession coclass. Use the Microsoft.Update.Session program identifier to create the object.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession">IUpdateSession</a>
