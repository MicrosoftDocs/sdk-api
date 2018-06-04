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

# FDE_SHAREVIOLATION_RESPONSE enumeration


## -description


Specifies the values used by the <a href="https://msdn.microsoft.com/bd9cfa69-4e55-48ca-915a-e5ecccf8bf96">IFileDialogEvents::OnShareViolation</a> method to indicate an application's response to a sharing violation that occurs when a file is opened or saved.


## -enum-fields




### -field FDESVR_DEFAULT

The application has not handled the event. The dialog displays a UI that indicates that the file is in use and a different file must be chosen.


### -field FDESVR_ACCEPT

The application has determined that the file should be returned from the dialog.


### -field FDESVR_REFUSE

The application has determined that the file should not be returned from the dialog.

