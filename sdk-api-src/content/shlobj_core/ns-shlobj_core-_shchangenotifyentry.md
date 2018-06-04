---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SHChangeNotifyEntry structure


## -description


Contains and receives information for change notifications. This structure is used with the <a href="https://msdn.microsoft.com/73143865-ca2f-4578-a7a2-2ba4833eddd8">SHChangeNotifyRegister</a> function and the <a href="https://msdn.microsoft.com/5d777115-bae3-47c4-9edc-c99c40a4f926">SFVM_QUERYFSNOTIFY</a> notification.


## -struct-fields




### -field pidl

Type: <b>PCIDLIST_ABSOLUTE</b>

PIDL for which to receive notifications.


### -field fRecursive

Type: <b>BOOL</b>

A flag indicating whether to post notifications for children of this PIDL. For example, if the PIDL points to a folder, then file notifications would come from the folder's children if this flag was <b>TRUE</b>.

