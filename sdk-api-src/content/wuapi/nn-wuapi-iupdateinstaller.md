---
UID: NN:wuapi.IUpdateInstaller
title: IUpdateInstaller (wuapi.h)
description: Installs or uninstalls updates from or onto a computer.
helpviewer_keywords: ["IUpdateInstaller","IUpdateInstaller interface [Windows Update Agent]","IUpdateInstaller interface [Windows Update Agent]","described","IUpdateInstaller interface [Windows Update Services]","IUpdateInstaller interface [Windows Update Services]","described","wua.iupdateinstaller","wuapi/IUpdateInstaller"]
old-location: wua\iupdateinstaller.htm
tech.root: wua
ms.assetid: 7f1c272f-73ef-43ee-b1ac-ef97a4791313
ms.date: 12/05/2018
ms.keywords: IUpdateInstaller, IUpdateInstaller interface [Windows Update Agent], IUpdateInstaller interface [Windows Update Agent],described, IUpdateInstaller interface [Windows Update Services], IUpdateInstaller interface [Windows Update Services],described, wua.iupdateinstaller, wuapi/IUpdateInstaller
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
 - IUpdateInstaller
 - wuapi/IUpdateInstaller
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
 - IUpdateInstaller
---

# IUpdateInstaller interface


## -description

Installs or uninstalls updates from or onto a computer.

## -inheritance

The <b>IUpdateInstaller</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUpdateInstaller</b> also has these types of members:

## -remarks

This interface can be instantiated by using the UpdateInstaller coclass. Use the Microsoft.Update.Installer program identifier to create the object.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller2">IUpdateInstaller2</a>
