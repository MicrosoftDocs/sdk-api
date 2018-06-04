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

# PrintDocumentPackageCompletion enumeration


## -description


The PrintDocumentPackageCompletion enumeration specifies the status of the print operation.


## -enum-fields




### -field PrintDocumentPackageCompletion_InProgress

The print job is running.


### -field PrintDocumentPackageCompletion_Completed

The print operation completed without error.


### -field PrintDocumentPackageCompletion_Canceled

The print operation was canceled.


### -field PrintDocumentPackageCompletion_Failed

The print operation failed.

