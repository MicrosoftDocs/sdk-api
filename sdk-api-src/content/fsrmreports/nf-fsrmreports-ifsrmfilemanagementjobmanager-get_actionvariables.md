---
UID: NF:fsrmreports.IFsrmFileManagementJobManager.get_ActionVariables
title: IFsrmFileManagementJobManager::get_ActionVariables
author: windows-sdk-content
description: Retrieves a list of macros that you can specify in action property values.
old-location: fsrm\ifsrmfilemanagementjobmanager_actionvariables.htm
tech.root: fsrm
ms.assetid: 222c826f-0ade-4e5d-be2e-5c0dfa8758d0
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ActionVariables property [File Server Resource Manager], ActionVariables property [File Server Resource Manager],FsrmFileManagementJobManager class, ActionVariables property [File Server Resource Manager],IFsrmFileManagementJobManager interface, FsrmFileManagementJobManager class [File Server Resource Manager],ActionVariables property, IFsrmFileManagementJobManager interface [File Server Resource Manager],ActionVariables property, IFsrmFileManagementJobManager.ActionVariables, IFsrmFileManagementJobManager.get_ActionVariables, IFsrmFileManagementJobManager::ActionVariables, IFsrmFileManagementJobManager::get_ActionVariables, fs.ifsrmfilemanagementjobmanager_actionvariables, fsrm.ifsrmfilemanagementjobmanager_actionvariables, fsrmreports/IFsrmFileManagementJobManager::ActionVariables, fsrmreports/IFsrmFileManagementJobManager::get_ActionVariables, get_ActionVariables
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: fsrmreports.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileManagementJobManager.ActionVariables
 - IFsrmFileManagementJobManager.get_ActionVariables
 - FsrmFileManagementJobManager.ActionVariables
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileManagementJobManager::get_ActionVariables


## -description


Retrieves a  list of macros that you can specify in action property values.

This property is read-only.


## -parameters


## -remarks



FSRM parses the action property for the macros and substitutes the macro string with the values that are specific to the event and computer on which the action occurred.




## -see-also




<a href="https://msdn.microsoft.com/f59844ba-2aff-4885-b80b-82f3e1a638d3">FsrmFileManagementJobManager</a>



<a href="https://msdn.microsoft.com/2df0e8d0-1da7-422e-8d02-ad5d030fdd8d">IFsrmFileManagementJobManager</a>
 

 

