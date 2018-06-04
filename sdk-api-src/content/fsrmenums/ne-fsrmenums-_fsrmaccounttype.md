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

# _FsrmAccountType enumeration


## -description


Defines the computer account types under which a command action (see 
    <a href="https://msdn.microsoft.com/3e34395e-b8e6-4288-a040-dff6cf7f5fe6">FsrmActionType</a>) can run.


## -enum-fields




### -field FsrmAccountType_Unknown

The account type is unknown. Do not use this value to set the 
      <a href="https://msdn.microsoft.com/24f0bf5c-064c-4f1e-b69f-23374ea78324">IFsrmActionCommand::Account</a> property.


### -field FsrmAccountType_NetworkService

Run the command or pipeline module under the "NetworkService" account.


### -field FsrmAccountType_LocalService

Run the command or pipeline module under the "LocalService" account.


### -field FsrmAccountType_LocalSystem

Run the command or pipeline module under the "LocalSystem" account.


### -field FsrmAccountType_InProc

This value is reserved for internal use.


### -field FsrmAccountType_External

Run the classifier or storage module in a separate process from FSRM (FSRM uses 
      <b>CLSCTX_LOCAL_SERVER</b> to instantiate the module). The module's COM registration 
      specifies the account used to run the module. If the registration does not specify the account, the module is 
      run using the user's account.


### -field FsrmAccountType_Automatic

Run the command or pipeline module under the account that FSRM selects. This is the recommended value.

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This enumeration value is not supported before Windows Server 2012.


## -see-also




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>



<a href="https://msdn.microsoft.com/3e34395e-b8e6-4288-a040-dff6cf7f5fe6">FsrmActionType</a>



<a href="https://msdn.microsoft.com/24f0bf5c-064c-4f1e-b69f-23374ea78324">IFsrmActionCommand.Account</a>



<a href="https://msdn.microsoft.com/8f50bd88-ad16-49a4-b9d8-6c71ef6d9620">IFsrmPipelineModuleDefinition.Account</a>
 

 

