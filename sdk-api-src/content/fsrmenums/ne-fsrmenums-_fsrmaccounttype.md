---
UID: NE:fsrmenums._FsrmAccountType
title: "_FsrmAccountType"
author: windows-sdk-content
description: Defines the computer account types under which a command action (see FsrmActionType) can run.
old-location: fsrm\fsrmaccounttype.htm
old-project: Fsrm
ms.assetid: 8df04b24-e3dd-46ee-8d06-6a3763946fbe
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: FsrmAccountType, FsrmAccountType enumeration [File Server Resource Manager], FsrmAccountType_Automatic, FsrmAccountType_External, FsrmAccountType_InProc, FsrmAccountType_LocalService, FsrmAccountType_LocalSystem, FsrmAccountType_NetworkService, FsrmAccountType_Unknown, _FsrmAccountType, fs.fsrmaccounttype, fsrm.fsrmaccounttype, fsrmenums/FsrmAccountType, fsrmenums/FsrmAccountType_Automatic, fsrmenums/FsrmAccountType_External, fsrmenums/FsrmAccountType_InProc, fsrmenums/FsrmAccountType_LocalService, fsrmenums/FsrmAccountType_LocalSystem, fsrmenums/FsrmAccountType_NetworkService, fsrmenums/FsrmAccountType_Unknown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmEnums.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FsrmAccountType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmAccountType
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
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
 

 

