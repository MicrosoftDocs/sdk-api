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

# FDE_OVERWRITE_RESPONSE enumeration


## -description


Specifies the values used by the <a href="https://msdn.microsoft.com/825dcbed-3248-4d2e-bf5f-5d51f8f0529b">IFileDialogEvents::OnOverwrite</a> method to indicate an application's response to an overwrite request during a save operation using the common file dialog.


## -enum-fields




### -field FDEOR_DEFAULT

The application has not handled the event. The dialog displays a UI asking the user whether the file should be overwritten and returned from the dialog.


### -field FDEOR_ACCEPT

The application has determined that the file should be returned from the dialog.


### -field FDEOR_REFUSE

The application has determined that the file should not be returned from the dialog.

