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

# IWsbApplicationBackupSupport::CheckConsistency


## -description


Checks the consistency of the VSS writer's components in the shadow copy after shadow copies are created 
   for the volumes to be backed up.


## -parameters




### -param wszWriterMetadata [in, optional]

A string that contains the VSS writer's metadata.


### -param wszComponentName [in, optional]

The name of the component or component set to be checked. This should match the name in the metadata that 
    the <i>wszWriterMetadata</i> parameter points to.


### -param wszComponentLogicalPath [in, optional]

The <a href="https://msdn.microsoft.com/663c8ca9-8f5b-48bd-af2d-b2d90de9e492">logical path</a> of the component or 
    component set to be checked. This should match the logical path in the metadata that the 
  <i>wszWriterMetadata</i> parameter points to.


### -param cVolumes [in]

The number of shadow copy volumes. The value of this parameter can range from 0 to 
    <b>MAX_VOLUMES</b>.


### -param rgwszSourceVolumePath [in, optional]

A pointer to an array of volume <b>GUID</b> paths, one for each of the source 
    volumes. The format of a volume <b>GUID</b> path is 
  "\\?\<i>Volume</i>{<i>GUID</i>}\".


### -param rgwszSnapshotVolumePath [in, optional]

A pointer to an array of volume <b>GUID</b> paths, one for each of the shadow copy 
    volumes. The consistency check is performed on these volumes.


### -param ppAsync [out, optional]

A pointer to a variable that will receive an 
    <a href="https://msdn.microsoft.com/cd8f74c0-c2dc-487c-b702-1e1355e99b7d">IWsbApplicationAsync</a> interface pointer that can be 
  used to retrieve the status of the consistency-check operation.  This pointer can be <b>NULL</b> 
  if a consistency check is not required. When the consistency-check operation is complete, the 
  <a href="_com_iunknown_release">IUnknown::Release</a> method must be called to free all 
      resources held by the <b>IWsbApplicationAsync</b> object.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise. Possible return values 
    include the following.




## -remarks



The application should perform the consistency check as an asynchronous operation, because it might be a 
  long-running operation. The application should check the consistency of the files for the VSS writer's components in 
  the shadow copy. These files will be backed up as part of the backup operation. If the consistency check fails, the 
  backup of the components will still succeed, but recovery of the components will not be allowed from the resulting 
  backup set.




## -see-also




<a href="https://msdn.microsoft.com/45865f1b-0f0a-46fc-b1f3-f2fd7c49f56f">IWsbApplicationBackupSupport</a>
 

 

