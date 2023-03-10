---
UID: NF:wuapi.IUpdateInstaller.get_ParentHwnd
title: IUpdateInstaller::get_ParentHwnd (wuapi.h)
description: Gets and sets a handle to the parent window that can contain a dialog box. (Get)
helpviewer_keywords: ["IUpdateInstaller interface [Windows Update Agent]","ParentHwnd property","IUpdateInstaller.ParentHwnd","IUpdateInstaller.get_ParentHwnd","IUpdateInstaller::ParentHwnd","IUpdateInstaller::get_ParentHwnd","IUpdateInstaller::put_ParentHwnd","ParentHwnd property [Windows Update Agent]","ParentHwnd property [Windows Update Agent]","IUpdateInstaller interface","get_ParentHwnd","wua.iupdateinstaller_parenthwnd","wuapi/IUpdateInstaller::ParentHwnd","wuapi/IUpdateInstaller::get_ParentHwnd","wuapi/IUpdateInstaller::put_ParentHwnd"]
old-location: wua\iupdateinstaller_parenthwnd.htm
tech.root: wua
ms.assetid: 6862ad8c-e1fa-4880-8800-88f485b7cebf
ms.date: 12/05/2018
ms.keywords: IUpdateInstaller interface [Windows Update Agent],ParentHwnd property, IUpdateInstaller.ParentHwnd, IUpdateInstaller.get_ParentHwnd, IUpdateInstaller::ParentHwnd, IUpdateInstaller::get_ParentHwnd, IUpdateInstaller::put_ParentHwnd, ParentHwnd property [Windows Update Agent], ParentHwnd property [Windows Update Agent],IUpdateInstaller interface, get_ParentHwnd, wua.iupdateinstaller_parenthwnd, wuapi/IUpdateInstaller::ParentHwnd, wuapi/IUpdateInstaller::get_ParentHwnd, wuapi/IUpdateInstaller::put_ParentHwnd
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
 - IUpdateInstaller::get_ParentHwnd
 - wuapi/IUpdateInstaller::get_ParentHwnd
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
 - IUpdateInstaller.ParentHwnd
 - IUpdateInstaller.get_ParentHwnd
 - IUpdateInstaller.put_ParentHwnd
---

# IUpdateInstaller::get_ParentHwnd


## -description

Gets and sets a handle to the parent window that can contain a dialog box.

This property is read/write.

## -parameters

## -remarks

This property can be changed only by a user on the computer. This property cannot be accessed by using the <b>IDispatch</b> interface.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a>
