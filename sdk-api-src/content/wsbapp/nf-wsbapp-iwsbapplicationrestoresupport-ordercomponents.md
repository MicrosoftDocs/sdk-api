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

# IWsbApplicationRestoreSupport::OrderComponents


## -description


Specifies the order in which application components are to be restored.


## -parameters




### -param cComponents [in]

The number of components to be restored. The value of this parameter can range from 0 to MAX_COMPONENTS.


### -param rgComponentName [in]

An array of <i>cComponents</i> names of components to be restored.


### -param rgComponentLogicalPaths [in]

An array of <i>cComponents</i> logical paths of components to be restored.


### -param prgComponentName [out]

An array of <i>cComponents</i> names of components to be restored,  in the order in which they are to be restored. This parameter receives <b>NULL</b> if no specific restore order is required.


### -param prgComponentLogicalPath [out]

An array of <i>cComponents</i> logical paths of components to be restored, in the order in which they are to be restored. This parameter receives <b>NULL</b> if no specific restore order is required.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise. Possible return values include the following.




## -remarks



Windows Server Backup calls this  method before restoring components for an application.




## -see-also




<a href="https://msdn.microsoft.com/694f9b4d-0ca8-4dbe-829c-6ac18c9aa140">IWsbApplicationRestoreSupport</a>
 

 

