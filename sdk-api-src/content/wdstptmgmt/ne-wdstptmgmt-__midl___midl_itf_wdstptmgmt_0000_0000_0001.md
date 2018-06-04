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

# __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0001 enumeration


## -description


Indicates which WDS features are installed on the WDS server.


## -enum-fields




### -field WdsTptFeatureAdminPack

The server has the WDS administrator pack installed. This feature is used for managing WDS local or remote WDS servers.


### -field WdsTptFeatureTransportServer

The server has the WDS Transport Server role installed. This feature provides a generic, extensible transport platform that can be used by any application. Generally, this role has to be installed on the server for most of the WdsTptMgmt functionality to be available. Without this role, only limited functionality about the server's install state would be available through WdsTptMgmt.


### -field WdsTptFeatureDeploymentServer

The server has the WDS Deployment Server role installed. This feature allows administrators to add operating system images to the server and configure it to allow PXE-booting clients to enumerate and install these images.

