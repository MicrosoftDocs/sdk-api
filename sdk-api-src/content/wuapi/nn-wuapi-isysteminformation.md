---
UID: NN:wuapi.ISystemInformation
title: ISystemInformation (wuapi.h)
description: Contains information about the specified computer. This information is relevant to the Windows Update Agent (WUA).
helpviewer_keywords: ["ISystemInformation","ISystemInformation interface [Windows Update Agent]","ISystemInformation interface [Windows Update Agent]","described","wua.isysteminformation","wuapi/ISystemInformation"]
old-location: wua\isysteminformation.htm
tech.root: wua
ms.assetid: b0aebfd6-1d62-43b3-8c40-2eeb67fab27d
ms.date: 12/05/2018
ms.keywords: ISystemInformation, ISystemInformation interface [Windows Update Agent], ISystemInformation interface [Windows Update Agent],described, wua.isysteminformation, wuapi/ISystemInformation
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
 - ISystemInformation
 - wuapi/ISystemInformation
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
 - ISystemInformation
---

# ISystemInformation interface


## -description

Contains information about the specified computer. This information is relevant to the Windows Update Agent (WUA).

## -remarks

You can create an instance of this interface by using the SystemInformation coclass. Use the Microsoft.Update.SystemInfo program identifier to create the object.

