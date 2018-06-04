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

# ASSOCDATA enumeration


## -description


Used by <a href="https://msdn.microsoft.com/7f21e564-97c6-4f9d-a4fa-160b78dbfc2f">IQueryAssociations::GetData</a> to define the type of data that is to be returned.


## -enum-fields




### -field ASSOCDATA_MSIDESCRIPTOR

The component descriptor to pass to the Windows Installer API.


### -field ASSOCDATA_NOACTIVATEHANDLER

Attempts to activate a window are restricted. There is no data associated with this value.


### -field ASSOCDATA_UNUSED1


### -field ASSOCDATA_HASPERUSERASSOC

Defaults to user specified association.


### -field ASSOCDATA_EDITFLAGS

<b>Internet Explorer version 6 or later</b>. Gets the data stored in the EditFlags value of a file association <a href="https://msdn.microsoft.com/f2b666d6-bf22-47b5-87e1-8de5ff51c152">PROGID</a> registry key. This value consists of one or more <a href="https://msdn.microsoft.com/63b58659-9c4c-4b39-98d1-743724523dcd">FILETYPEATTRIBUTEFLAGS</a>. Compare against those values to determine which attributes have been set.


### -field ASSOCDATA_VALUE

<b>Internet Explorer version 6 or later</b>. Uses the <i>pwszExtra</i> parameter from the <a href="https://msdn.microsoft.com/7f21e564-97c6-4f9d-a4fa-160b78dbfc2f">IQueryAssociations::GetData</a> method as the value name.


### -field ASSOCDATA_MAX




#### - ASSOCDATA_QUERYCLASSSTORE

If this value is present, applications should check the Windows 2000 class store.

