---
UID: NF:fsrm.IFsrmActionCommand.get_ExecutablePath
title: IFsrmActionCommand::get_ExecutablePath (fsrm.h)
description: Retrieves or sets the full path to the executable program or script to run. (Get)
helpviewer_keywords: ["ExecutablePath property [File Server Resource Manager]","ExecutablePath property [File Server Resource Manager]","IFsrmActionCommand interface","IFsrmActionCommand interface [File Server Resource Manager]","ExecutablePath property","IFsrmActionCommand.ExecutablePath","IFsrmActionCommand.get_ExecutablePath","IFsrmActionCommand::ExecutablePath","IFsrmActionCommand::get_ExecutablePath","IFsrmActionCommand::put_ExecutablePath","fs.ifsrmactioncommand_executablepath","fsrm.ifsrmactioncommand_executablepath","fsrm/IFsrmActionCommand::ExecutablePath","fsrm/IFsrmActionCommand::get_ExecutablePath","fsrm/IFsrmActionCommand::put_ExecutablePath","get_ExecutablePath"]
old-location: fsrm\ifsrmactioncommand_executablepath.htm
tech.root: fsrm
ms.assetid: c15b09e3-a8b6-4c73-82d7-8de7c2635f77
ms.date: 12/05/2018
ms.keywords: ExecutablePath property [File Server Resource Manager], ExecutablePath property [File Server Resource Manager],IFsrmActionCommand interface, IFsrmActionCommand interface [File Server Resource Manager],ExecutablePath property, IFsrmActionCommand.ExecutablePath, IFsrmActionCommand.get_ExecutablePath, IFsrmActionCommand::ExecutablePath, IFsrmActionCommand::get_ExecutablePath, IFsrmActionCommand::put_ExecutablePath, fs.ifsrmactioncommand_executablepath, fsrm.ifsrmactioncommand_executablepath, fsrm/IFsrmActionCommand::ExecutablePath, fsrm/IFsrmActionCommand::get_ExecutablePath, fsrm/IFsrmActionCommand::put_ExecutablePath, get_ExecutablePath
req.header: fsrm.h
req.include-header: FsrmQuota.h, FsrmScreen.h
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
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmActionCommand::get_ExecutablePath
 - fsrm/IFsrmActionCommand::get_ExecutablePath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmActionCommand.ExecutablePath
 - IFsrmActionCommand.get_ExecutablePath
 - IFsrmActionCommand.put_ExecutablePath
---

# IFsrmActionCommand::get_ExecutablePath


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets the full path to the executable program or script to run.

This property is read/write.

## -parameters

## -remarks

The path must exist at the time you set the property and when the command executes. If the path does not exist 
    when the command executes, FSRM writes an event to the Application log.

To execute the command, the user that configured the action must exist in the Administrators group at the time 
    the command is executed.

Only administrators can have write access to all folders in the path at the time you set the property and when 
    the command executes. If others have write access when the command executes, FSRM does not execute the command and 
    writes an event to the Application log.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>
