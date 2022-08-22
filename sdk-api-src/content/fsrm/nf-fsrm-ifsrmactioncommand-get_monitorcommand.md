---
UID: NF:fsrm.IFsrmActionCommand.get_MonitorCommand
title: IFsrmActionCommand::get_MonitorCommand (fsrm.h)
description: Retrieves or sets a value that determines whether FSRM will monitor the executable program specified in the ExecutablePath property. (Get)
helpviewer_keywords: ["IFsrmActionCommand interface [File Server Resource Manager]","MonitorCommand property","IFsrmActionCommand.MonitorCommand","IFsrmActionCommand.get_MonitorCommand","IFsrmActionCommand::MonitorCommand","IFsrmActionCommand::get_MonitorCommand","IFsrmActionCommand::put_MonitorCommand","MonitorCommand property [File Server Resource Manager]","MonitorCommand property [File Server Resource Manager]","IFsrmActionCommand interface","fs.ifsrmactioncommand_monitorcommand","fsrm.ifsrmactioncommand_monitorcommand","fsrm/IFsrmActionCommand::MonitorCommand","fsrm/IFsrmActionCommand::get_MonitorCommand","fsrm/IFsrmActionCommand::put_MonitorCommand","get_MonitorCommand"]
old-location: fsrm\ifsrmactioncommand_monitorcommand.htm
tech.root: fsrm
ms.assetid: 7aa420de-9be5-4333-a511-23e0443e633b
ms.date: 12/05/2018
ms.keywords: IFsrmActionCommand interface [File Server Resource Manager],MonitorCommand property, IFsrmActionCommand.MonitorCommand, IFsrmActionCommand.get_MonitorCommand, IFsrmActionCommand::MonitorCommand, IFsrmActionCommand::get_MonitorCommand, IFsrmActionCommand::put_MonitorCommand, MonitorCommand property [File Server Resource Manager], MonitorCommand property [File Server Resource Manager],IFsrmActionCommand interface, fs.ifsrmactioncommand_monitorcommand, fsrm.ifsrmactioncommand_monitorcommand, fsrm/IFsrmActionCommand::MonitorCommand, fsrm/IFsrmActionCommand::get_MonitorCommand, fsrm/IFsrmActionCommand::put_MonitorCommand, get_MonitorCommand
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
 - IFsrmActionCommand::get_MonitorCommand
 - fsrm/IFsrmActionCommand::get_MonitorCommand
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
 - IFsrmActionCommand.MonitorCommand
 - IFsrmActionCommand.get_MonitorCommand
 - IFsrmActionCommand.put_MonitorCommand
---

# IFsrmActionCommand::get_MonitorCommand


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets a value that determines whether FSRM will monitor the executable program specified 
    in the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioncommand-get_executablepath">ExecutablePath</a> 
    property.

This property is read/write.

## -parameters

## -remarks

The <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioncommand-get_killtimeout">KillTimeOut</a> and 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioncommand-get_logresult">LogResult</a> properties are ignored if this 
    property is not set to <b>VARIANT_TRUE</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioncommand-get_logresult">IFsrmActionCommand::LogResult</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>
