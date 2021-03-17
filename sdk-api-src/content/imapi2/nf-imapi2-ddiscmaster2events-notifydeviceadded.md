---
UID: NF:imapi2.DDiscMaster2Events.NotifyDeviceAdded
title: DDiscMaster2Events::NotifyDeviceAdded (imapi2.h)
description: Receives notification when an optical media device is added to the computer.
helpviewer_keywords: ["DDiscMaster2Events interface [IMAPI]","NotifyDeviceAdded method","DDiscMaster2Events.NotifyDeviceAdded","DDiscMaster2Events::NotifyDeviceAdded","NotifyDeviceAdded","NotifyDeviceAdded method [IMAPI]","NotifyDeviceAdded method [IMAPI]","DDiscMaster2Events interface","imapi.ddiscmaster2events_notifydeviceadded","imapi2/DDiscMaster2Events::NotifyDeviceAdded"]
old-location: imapi\ddiscmaster2events_notifydeviceadded.htm
tech.root: imapi
ms.assetid: 1f728b33-3788-4fc4-b261-da243b4ff46e
ms.date: 12/05/2018
ms.keywords: DDiscMaster2Events interface [IMAPI],NotifyDeviceAdded method, DDiscMaster2Events.NotifyDeviceAdded, DDiscMaster2Events::NotifyDeviceAdded, NotifyDeviceAdded, NotifyDeviceAdded method [IMAPI], NotifyDeviceAdded method [IMAPI],DDiscMaster2Events interface, imapi.ddiscmaster2events_notifydeviceadded, imapi2/DDiscMaster2Events::NotifyDeviceAdded
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
 - DDiscMaster2Events::NotifyDeviceAdded
 - imapi2/DDiscMaster2Events::NotifyDeviceAdded
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
 - DDiscMaster2Events.NotifyDeviceAdded
---

# DDiscMaster2Events::NotifyDeviceAdded


## -description

Receives notification when an optical media device is added to the computer.

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