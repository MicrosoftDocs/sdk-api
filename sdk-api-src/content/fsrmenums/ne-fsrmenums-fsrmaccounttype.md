---
UID: NE:fsrmenums._FsrmAccountType
title: FsrmAccountType (fsrmenums.h)
description: Defines the computer account types under which a command action (see FsrmActionType) can run.
helpviewer_keywords: ["FsrmAccountType","FsrmAccountType enumeration [File Server Resource Manager]","FsrmAccountType_Automatic","FsrmAccountType_External","FsrmAccountType_InProc","FsrmAccountType_LocalService","FsrmAccountType_LocalSystem","FsrmAccountType_NetworkService","FsrmAccountType_Unknown","fs.fsrmaccounttype","fsrm.fsrmaccounttype","fsrmenums/FsrmAccountType","fsrmenums/FsrmAccountType_Automatic","fsrmenums/FsrmAccountType_External","fsrmenums/FsrmAccountType_InProc","fsrmenums/FsrmAccountType_LocalService","fsrmenums/FsrmAccountType_LocalSystem","fsrmenums/FsrmAccountType_NetworkService","fsrmenums/FsrmAccountType_Unknown"]
old-location: fsrm\fsrmaccounttype.htm
tech.root: fsrm
ms.assetid: 8df04b24-e3dd-46ee-8d06-6a3763946fbe
ms.date: 12/05/2018
ms.keywords: FsrmAccountType, FsrmAccountType enumeration [File Server Resource Manager], FsrmAccountType_Automatic, FsrmAccountType_External, FsrmAccountType_InProc, FsrmAccountType_LocalService, FsrmAccountType_LocalSystem, FsrmAccountType_NetworkService, FsrmAccountType_Unknown, fs.fsrmaccounttype, fsrm.fsrmaccounttype, fsrmenums/FsrmAccountType, fsrmenums/FsrmAccountType_Automatic, fsrmenums/FsrmAccountType_External, fsrmenums/FsrmAccountType_InProc, fsrmenums/FsrmAccountType_LocalService, fsrmenums/FsrmAccountType_LocalSystem, fsrmenums/FsrmAccountType_NetworkService, fsrmenums/FsrmAccountType_Unknown
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
targetos: Windows
req.typenames: FsrmAccountType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmAccountType
 - fsrmenums/_FsrmAccountType
 - FsrmAccountType
 - fsrmenums/FsrmAccountType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmAccountType
---

# FsrmAccountType enumeration


## -description

Defines the computer account types under which a command action (see 
    <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmactiontype">FsrmActionType</a>) can run.

## -enum-fields

### -field FsrmAccountType_Unknown:0

The account type is unknown. Do not use this value to set the 
      <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioncommand-get_account">IFsrmActionCommand::Account</a> property.

### -field FsrmAccountType_NetworkService:1

Run the command or pipeline module under the "NetworkService" account.

### -field FsrmAccountType_LocalService:2

Run the command or pipeline module under the "LocalService" account.

### -field FsrmAccountType_LocalSystem:3

Run the command or pipeline module under the "LocalSystem" account.

### -field FsrmAccountType_InProc:4

This value is reserved for internal use.

### -field FsrmAccountType_External:5

Run the classifier or storage module in a separate process from FSRM (FSRM uses 
      <b>CLSCTX_LOCAL_SERVER</b> to instantiate the module). The module's COM registration 
      specifies the account used to run the module. If the registration does not specify the account, the module is 
      run using the user's account.

### -field FsrmAccountType_Automatic:500

Run the command or pipeline module under the account that FSRM selects. This is the recommended value.

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This enumeration value is not supported before Windows Server 2012.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>



<a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmactiontype">FsrmActionType</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioncommand-get_account">IFsrmActionCommand.Account</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpipelinemoduledefinition-get_account">IFsrmPipelineModuleDefinition.Account</a>
