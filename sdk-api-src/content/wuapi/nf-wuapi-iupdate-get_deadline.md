---
UID: NF:wuapi.IUpdate.get_Deadline
title: IUpdate::get_Deadline (wuapi.h)
description: Gets the date by which the update must be installed.
helpviewer_keywords: ["Deadline property [Windows Update Agent]","Deadline property [Windows Update Agent]","IUpdate interface","IUpdate interface [Windows Update Agent]","Deadline property","IUpdate.Deadline","IUpdate.get_Deadline","IUpdate::Deadline","IUpdate::get_Deadline","get_Deadline","wua.iupdate_deadline","wuapi/IUpdate::Deadline","wuapi/IUpdate::get_Deadline"]
old-location: wua\iupdate_deadline.htm
tech.root: wua
ms.assetid: 78f5ab06-13d1-4564-b9eb-334d4f0c34e8
ms.date: 12/05/2018
ms.keywords: Deadline property [Windows Update Agent], Deadline property [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],Deadline property, IUpdate.Deadline, IUpdate.get_Deadline, IUpdate::Deadline, IUpdate::get_Deadline, get_Deadline, wua.iupdate_deadline, wuapi/IUpdate::Deadline, wuapi/IUpdate::get_Deadline
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
 - IUpdate::get_Deadline
 - wuapi/IUpdate::get_Deadline
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
 - IUpdate.Deadline
 - IUpdate.get_Deadline
---

# IUpdate::get_Deadline


## -description

Gets the date by which the update must be installed.

This property is read-only.

## -parameters

## -remarks

In COM, if the update has a deadline, the return value is of type VT_DATE and contains a DATE value that specifies the deadline. Otherwise, the return value is of type VT_EMPTY.

In the Microsoft .NET Framework, the return value is <b>NULL</b> if the update has no deadline.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>