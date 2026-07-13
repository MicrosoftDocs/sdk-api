---
UID: NN:wuapi.IUpdateSession
title: IUpdateSession (wuapi.h)
description: Represents a session in which the caller can perform operations that involve updates. For example, this interface represents sessions in which the caller performs a search, download, installation, or uninstallation operation. (IUpdateSession)
helpviewer_keywords: ["IUpdateSession","IUpdateSession interface [Windows Update Agent]","IUpdateSession interface [Windows Update Agent]","described","wua.iupdatesession","wuapi/IUpdateSession"]
old-location: wua\iupdatesession.htm
tech.root: wua
ms.assetid: 00b84246-b5f2-48c2-a0ab-eaaa1ec80262
ms.date: 12/05/2018
ms.keywords: IUpdateSession, IUpdateSession interface [Windows Update Agent], IUpdateSession interface [Windows Update Agent],described, wua.iupdatesession, wuapi/IUpdateSession
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
 - IUpdateSession
 - wuapi/IUpdateSession
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
 - IUpdateSession
---

# IUpdateSession interface


## -description

Represents a session in which the caller can perform operations that involve updates. For example, this interface represents sessions in which the caller performs a search, download, installation, or uninstallation operation.

## -inheritance

The <b>IUpdateSession</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUpdateSession</b> also has these types of members:

## -remarks

You can create an instance of this interface by using the UpdateSession coclass. Use the Microsoft.Update.Session program identifier to create the object.
