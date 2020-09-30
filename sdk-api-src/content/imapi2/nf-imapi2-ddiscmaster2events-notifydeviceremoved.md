---
UID: NF:imapi2.DDiscMaster2Events.NotifyDeviceRemoved
title: DDiscMaster2Events::NotifyDeviceRemoved (imapi2.h)
description: Receives notification when an optical media device is removed from the computer.
helpviewer_keywords: ["DDiscMaster2Events interface [IMAPI]","NotifyDeviceRemoved method","DDiscMaster2Events.NotifyDeviceRemoved","DDiscMaster2Events::NotifyDeviceRemoved","NotifyDeviceRemoved","NotifyDeviceRemoved method [IMAPI]","NotifyDeviceRemoved method [IMAPI]","DDiscMaster2Events interface","imapi.ddiscmaster2events_notifydeviceremoved","imapi2/DDiscMaster2Events::NotifyDeviceRemoved"]
old-location: imapi\ddiscmaster2events_notifydeviceremoved.htm
tech.root: imapi
ms.assetid: 626096ba-f2d7-4a75-b04c-f95aad6915cc
ms.date: 12/05/2018
ms.keywords: DDiscMaster2Events interface [IMAPI],NotifyDeviceRemoved method, DDiscMaster2Events.NotifyDeviceRemoved, DDiscMaster2Events::NotifyDeviceRemoved, NotifyDeviceRemoved, NotifyDeviceRemoved method [IMAPI], NotifyDeviceRemoved method [IMAPI],DDiscMaster2Events interface, imapi.ddiscmaster2events_notifydeviceremoved, imapi2/DDiscMaster2Events::NotifyDeviceRemoved
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DDiscMaster2Events::NotifyDeviceRemoved
 - imapi2/DDiscMaster2Events::NotifyDeviceRemoved
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - DDiscMaster2Events.NotifyDeviceRemoved
---

# DDiscMaster2Events::NotifyDeviceRemoved


## -description

Receives notification when an optical media device is removed from the computer.

## -parameters

### -param object [in]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2">IDiscMaster2</a> interface that you can use to enumerate the devices on the computer. 

This parameter is a <b>MsftDiscMaster2</b> object in script.

### -param uniqueId [in]

String that contains an identifier that uniquely identifies the optical media device that was added to the computer.

## -returns

Return values are ignored.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events">DDiscMaster2Events</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2">IDiscMaster2</a>