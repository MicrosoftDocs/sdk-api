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

# IWsbApplicationRestoreSupport::PostRestore


## -description


Performs application-specific <a href="https://msdn.microsoft.com/44279c0e-17f4-4109-bc12-af9064cd321e">PostRestore</a> operations.


## -parameters




### -param wszWriterMetadata [in, optional]

A string that contains the VSS writer's metadata.


### -param wszComponentName [in, optional]

The name of the component or component set. This should match the name in the metadata that the <i>wszWriterMetadata</i> parameter points to.


### -param wszComponentLogicalPath [in, optional]

The <a href="https://msdn.microsoft.com/663c8ca9-8f5b-48bd-af2d-b2d90de9e492">logical path</a> of the component or component set. This should match the logical path in the metadata that the <i>wszWriterMetadata</i> parameter points to.


### -param bNoRollForward [in]

Set to <b>TRUE</b> if a previous point-in-time recovery operation is in progress and no application rollforward should be performed. The previous logs for the application will be deleted before the application restore operation is performed.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise. Possible return values include the following.




## -remarks



During application restore, Windows Server Backup calls this method after restoring the files for each application component.




## -see-also




<a href="https://msdn.microsoft.com/694f9b4d-0ca8-4dbe-829c-6ac18c9aa140">IWsbApplicationRestoreSupport</a>
 

 

