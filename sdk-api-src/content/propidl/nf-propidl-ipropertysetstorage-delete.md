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

# IPropertySetStorage::Delete


## -description



			The <b>Delete</b> method deletes one of the property sets contained in the property set storage object.


## -parameters




### -param rfmtid






#### - fmtid [in]

FMTID of the property set to be deleted.


## -returns



This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



<b>IPropertySetStorage::Delete</b> deletes the property set specified by its FMTID. Specifying a property set that does not exist returns an error. Open substorages and streams(opened through one of the storage- or stream-valued properties) are put into the reverted state.



