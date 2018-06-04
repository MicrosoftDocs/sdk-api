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

# FAX_SERVER_APIVERSION_ENUM enumeration


## -description


The <b>FAX_SERVER_APIVERSION_ENUM </b> enumeration defines the version of the fax API. No value below is supported on any version of the fax service earlier than the one it designates. 


## -enum-fields




### -field fsAPI_VERSION_0

API Version 0, the fax service API used by the BackOffice Small Business Server 2000 (SBS) and BackOffice Server 2000 (BOS). Not supported.


### -field fsAPI_VERSION_1

API Version 1, the fax service API used by the Windows XP fax service server.


### -field fsAPI_VERSION_2

API Version 2, the fax service API used by the Windows Server 2003 fax service server.


### -field fsAPI_VERSION_3

API Version 3, the fax service API used by the Windows Vista fax service server.

