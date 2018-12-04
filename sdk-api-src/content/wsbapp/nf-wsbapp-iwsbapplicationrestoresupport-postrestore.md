---
UID: NF:wsbapp.IWsbApplicationRestoreSupport.PostRestore
title: IWsbApplicationRestoreSupport::PostRestore
author: windows-sdk-content
description: Performs application-specific PostRestore operations.
old-location: wsb\iwsbapplicationrestoresupport_postrestore.htm
tech.root: wsb
ms.assetid: 8be7975e-9b94-4a6e-b1f5-794b8749ccbe
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWsbApplicationRestoreSupport interface [Windows Server Backup],PostRestore method, IWsbApplicationRestoreSupport.PostRestore, IWsbApplicationRestoreSupport::PostRestore, PostRestore, PostRestore method [Windows Server Backup], PostRestore method [Windows Server Backup],IWsbApplicationRestoreSupport interface, wsb.iwsbapplicationrestoresupport_postrestore, wsbapp/IWsbApplicationRestoreSupport::PostRestore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsbapp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsbApp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WsbApp.h
api_name:
 - IWsbApplicationRestoreSupport.PostRestore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

