---
UID: NF:imapi2.DDiscMaster2Events.NotifyDeviceRemoved
title: DDiscMaster2Events::NotifyDeviceRemoved
author: windows-sdk-content
description: Receives notification when an optical media device is removed from the computer.
old-location: imapi\ddiscmaster2events_notifydeviceremoved.htm
old-project: imapi
ms.assetid: 626096ba-f2d7-4a75-b04c-f95aad6915cc
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: DDiscMaster2Events interface [IMAPI],NotifyDeviceRemoved method, DDiscMaster2Events.NotifyDeviceRemoved, DDiscMaster2Events::NotifyDeviceRemoved, NotifyDeviceRemoved, NotifyDeviceRemoved method [IMAPI], NotifyDeviceRemoved method [IMAPI],DDiscMaster2Events interface, imapi.ddiscmaster2events_notifydeviceremoved, imapi2/DDiscMaster2Events::NotifyDeviceRemoved
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - DDiscMaster2Events.NotifyDeviceRemoved
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# DDiscMaster2Events::NotifyDeviceRemoved


## -description


Receives notification when an optical media device is removed from the computer.


## -parameters




### -param object [in]

An <a href="https://msdn.microsoft.com/cdca44d4-6ab5-4c2f-91ba-bef79b1d457e">IDiscMaster2</a> interface that you can use to enumerate the devices on the computer. 

This parameter is a <b>MsftDiscMaster2</b> object in script.


### -param uniqueId [in]

String that contains an identifier that uniquely identifies the optical media device that was added to the computer.


## -returns



Return values are ignored.




## -see-also




<a href="https://msdn.microsoft.com/f01fa2d8-989d-499f-b79d-495108640aa2">DDiscMaster2Events</a>



<a href="https://msdn.microsoft.com/cdca44d4-6ab5-4c2f-91ba-bef79b1d457e">IDiscMaster2</a>
 

 

