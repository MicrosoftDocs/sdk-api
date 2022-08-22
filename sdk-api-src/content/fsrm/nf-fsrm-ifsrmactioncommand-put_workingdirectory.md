---
UID: NF:fsrm.IFsrmActionCommand.put_WorkingDirectory
title: IFsrmActionCommand::put_WorkingDirectory (fsrm.h)
description: Retrieves or sets the working directory in which the executable program will run. (Put)
helpviewer_keywords: ["IFsrmActionCommand interface [File Server Resource Manager]","WorkingDirectory property","IFsrmActionCommand.WorkingDirectory","IFsrmActionCommand.put_WorkingDirectory","IFsrmActionCommand::WorkingDirectory","IFsrmActionCommand::get_WorkingDirectory","IFsrmActionCommand::put_WorkingDirectory","WorkingDirectory property [File Server Resource Manager]","WorkingDirectory property [File Server Resource Manager]","IFsrmActionCommand interface","fs.ifsrmactioncommand_workingdirectory","fsrm.ifsrmactioncommand_workingdirectory","fsrm/IFsrmActionCommand::WorkingDirectory","fsrm/IFsrmActionCommand::get_WorkingDirectory","fsrm/IFsrmActionCommand::put_WorkingDirectory","put_WorkingDirectory"]
old-location: fsrm\ifsrmactioncommand_workingdirectory.htm
tech.root: fsrm
ms.assetid: 6844b6c3-11b4-4544-bd4e-bf2b89af00b7
ms.date: 12/05/2018
ms.keywords: IFsrmActionCommand interface [File Server Resource Manager],WorkingDirectory property, IFsrmActionCommand.WorkingDirectory, IFsrmActionCommand.put_WorkingDirectory, IFsrmActionCommand::WorkingDirectory, IFsrmActionCommand::get_WorkingDirectory, IFsrmActionCommand::put_WorkingDirectory, WorkingDirectory property [File Server Resource Manager], WorkingDirectory property [File Server Resource Manager],IFsrmActionCommand interface, fs.ifsrmactioncommand_workingdirectory, fsrm.ifsrmactioncommand_workingdirectory, fsrm/IFsrmActionCommand::WorkingDirectory, fsrm/IFsrmActionCommand::get_WorkingDirectory, fsrm/IFsrmActionCommand::put_WorkingDirectory, put_WorkingDirectory
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
 - IFsrmActionCommand::put_WorkingDirectory
 - fsrm/IFsrmActionCommand::put_WorkingDirectory
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
 - IFsrmActionCommand.WorkingDirectory
 - IFsrmActionCommand.get_WorkingDirectory
 - IFsrmActionCommand.put_WorkingDirectory
---

# IFsrmActionCommand::put_WorkingDirectory


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets the working directory in which the executable program will run.

This property is read/write.

## -parameters

## -remarks

The path can contain environment variables.

The path must exist when you set the property or the command executes. If the path does not exist when the 
    command executes, FSRM writes an event to the Application log.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>
