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

# _NOTIFYCANCEL structure


## -description


The <b>NOTIFYCANCEL</b> structure contains the details of a network disconnect operation. It is used by the 
<a href="https://msdn.microsoft.com/94bd969d-f94d-449c-971d-d17fff2c07e1">CancelConnectNotify</a> function.


## -struct-fields




### -field lpName

Pointer to the name of the local device or network resource whose connection is being canceled.


### -field lpProvider

For advance notification, this field is not defined. The MPR will try all valid providers to cancel the connection. 




For after-the-fact notification, if the cancel operation was successful, this field specifies the name of the network provider that canceled the connection.


### -field dwFlags

Currently, the only flag supported is CONNECT_UPDATE_PROFILE, which indicates whether the disconnection should remain persistent. If this flag is set, Windows no longer restores this connection when the user logs on.


### -field fForce

Indicates whether the disconnect should continue even if there are open files or jobs on the connection. If this field is <b>TRUE</b>, the connection is canceled regardless of open files or jobs. If this field is <b>FALSE</b>, the connection will not be canceled if there are open files or jobs.

