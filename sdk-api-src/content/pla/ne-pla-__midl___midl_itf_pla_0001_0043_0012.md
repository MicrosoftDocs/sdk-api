---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0012
title: "__MIDL___MIDL_itf_pla_0001_0043_0012"
author: windows-sdk-content
description: Defines the action that the data manager takes when both the age and size limits are met.
old-location: pla\folderactionsteps.htm
tech.root: pla
ms.assetid: 94d199a1-36f7-4064-a4fb-90dd26c37960
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: FolderActionSteps, FolderActionSteps enumeration [PLA], __MIDL___MIDL_itf_pla_0001_0043_0012, base.folderactionsteps, pla.folderactionsteps, pla/FolderActionSteps, pla/plaCreateCab, pla/plaDeleteCab, pla/plaDeleteData, pla/plaDeleteReport, pla/plaSendCab, plaCreateCab, plaDeleteCab, plaDeleteData, plaDeleteReport, plaSendCab
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - FolderActionSteps
product: Windows
targetos: Windows
req.typenames: FolderActionSteps
req.redist: 
---

# __MIDL___MIDL_itf_pla_0001_0043_0012 enumeration


## -description


Defines the action that the data manager takes when both the age and size limits are met.


## -enum-fields




### -field plaCreateCab

Creates a cabinet file. The name of the cabinet file is  <i>nameofthesubfolder</i>.cab.


### -field plaDeleteData

Deletes all files in the folder, except the report and cabinet file.


### -field plaSendCab

Sends the cabinet file to the location specified in the <a href="https://msdn.microsoft.com/a6398d07-f15d-401b-a3b6-21b2506ad270">IFolderAction::SendCabTo</a> property.


### -field plaDeleteCab

Deletes the cabinet file.


### -field plaDeleteReport

Deletes the report file.


## -remarks



Specify one or more actions. The data manager applies the actions in the order in which they are defined in this enumeration.




## -see-also




<a href="https://msdn.microsoft.com/7e7672d9-9384-4365-aa4a-bf8dace050c2">IFolderAction::Actions</a>
 

 

