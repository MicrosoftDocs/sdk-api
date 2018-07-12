---
UID: NF:fsrmscreen.IFsrmFileScreenBase.CreateAction
title: IFsrmFileScreenBase::CreateAction
author: windows-sdk-content
description: Creates an action for this file screen object.
old-location: fsrm\ifsrmfilescreenbase_createaction.htm
old-project: fsrm
ms.assetid: 1d627e07-fa8c-4c22-acba-c08767b8ebaa
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: CreateAction, CreateAction method [File Server Resource Manager], CreateAction method [File Server Resource Manager],IFsrmFileScreenBase interface, IFsrmFileScreenBase interface [File Server Resource Manager],CreateAction method, IFsrmFileScreenBase.CreateAction, IFsrmFileScreenBase::CreateAction, fs.ifsrmfilescreenbase_createaction, fsrm.ifsrmfilescreenbase_createaction, fsrmscreen/IFsrmFileScreenBase::CreateAction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmscreen.h
req.include-header: FsrmScreen.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmScreen.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileScreenBase.CreateAction
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreenBase::CreateAction


## -description


Creates an action for this file screen object. The action is triggered when a file 
    violates the file screen.


## -parameters




### -param actionType [in]

The type of action to create. For possible values, see the 
      <a href="https://msdn.microsoft.com/3e34395e-b8e6-4288-a040-dff6cf7f5fe6">FsrmActionType</a> enumeration.


### -param action [out]

An <a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a> interface to the newly created action. 
      Query the interface for the specific action specified. For example, if <i>actionType</i> is 
      <b>FsrmActionType_Command</b>, query <i>action</i> for the 
      <a href="https://msdn.microsoft.com/b7f9fc8c-2f55-4a0e-879a-64c368abcabb">IFsrmActionCommand</a> interface.


## -returns



The method returns the following return values.




## -remarks



You can specify up to four unique actions for each file screen.

The action is deleted if the file screen is deleted.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/45b16b46-7c03-4af5-889f-64047ec5ca98">Performing Actions Based on File Screen Violations</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9e52af8c-e03b-4b44-83bd-541fe1419d6c">IFsrmFileScreenBase</a>
 

 

