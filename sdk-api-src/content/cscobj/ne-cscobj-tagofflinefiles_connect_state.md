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

# tagOFFLINEFILES_CONNECT_STATE enumeration


## -description


Describes the connection state of an item in the Offline Files cache.


## -enum-fields




### -field OFFLINEFILES_CONNECT_STATE_UNKNOWN

Returned by <a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">IOfflineFilesConnectionInfo::GetConnectState</a> if the method fails.


### -field OFFLINEFILES_CONNECT_STATE_OFFLINE

Returned by <a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">IOfflineFilesConnectionInfo::GetConnectState</a> if the item is offline. Pass this value to <a href="https://msdn.microsoft.com/42412f42-7a70-4110-88ec-a38b3df7d2da">IOfflineFilesConnectionInfo::SetConnectState</a> to transition the item to offline.


### -field OFFLINEFILES_CONNECT_STATE_ONLINE

Returned by <a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">IOfflineFilesConnectionInfo::GetConnectState</a> if the item is online. Pass this value to <a href="https://msdn.microsoft.com/42412f42-7a70-4110-88ec-a38b3df7d2da">IOfflineFilesConnectionInfo::SetConnectState</a> to transition the item to online.


### -field OFFLINEFILES_CONNECT_STATE_TRANSPARENTLY_CACHED

Returned by <a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">IOfflineFilesConnectionInfo::GetConnectState</a> if the item is transparently cached.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported before Windows Server 2008 R2 and Windows 7.


### -field OFFLINEFILES_CONNECT_STATE_PARTLY_TRANSPARENTLY_CACHED

Returned by <a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">IOfflineFilesConnectionInfo::GetConnectState</a> if the item contains both transparently cached data and data that can be made available offline.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported before Windows Server 2008 R2 and Windows 7.


## -remarks



Transparently cached data is accessible only when the client is connected to the server.




## -see-also




<a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">IOfflineFilesConnectionInfo::GetConnectState</a>



<a href="https://msdn.microsoft.com/42412f42-7a70-4110-88ec-a38b3df7d2da">IOfflineFilesConnectionInfo::SetConnectState</a>
 

 

