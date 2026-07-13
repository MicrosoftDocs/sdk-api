---
UID: NF:fsrm.IFsrmActionCommand.get_KillTimeOut
title: IFsrmActionCommand::get_KillTimeOut (fsrm.h)
description: Retrieves or sets the number of minutes the server waits before terminating the process that is running the executable program specified in the ExecutablePath property. (Get)
helpviewer_keywords: ["IFsrmActionCommand interface [File Server Resource Manager]","KillTimeOut property","IFsrmActionCommand.KillTimeOut","IFsrmActionCommand.get_KillTimeOut","IFsrmActionCommand::KillTimeOut","IFsrmActionCommand::get_KillTimeOut","IFsrmActionCommand::put_KillTimeOut","KillTimeOut property [File Server Resource Manager]","KillTimeOut property [File Server Resource Manager]","IFsrmActionCommand interface","fs.ifsrmactioncommand_killtimeout","fsrm.ifsrmactioncommand_killtimeout","fsrm/IFsrmActionCommand::KillTimeOut","fsrm/IFsrmActionCommand::get_KillTimeOut","fsrm/IFsrmActionCommand::put_KillTimeOut","get_KillTimeOut"]
old-location: fsrm\ifsrmactioncommand_killtimeout.htm
tech.root: fsrm
ms.assetid: 2873f1c4-6827-411f-b12f-9c282cf91119
ms.date: 12/05/2018
ms.keywords: IFsrmActionCommand interface [File Server Resource Manager],KillTimeOut property, IFsrmActionCommand.KillTimeOut, IFsrmActionCommand.get_KillTimeOut, IFsrmActionCommand::KillTimeOut, IFsrmActionCommand::get_KillTimeOut, IFsrmActionCommand::put_KillTimeOut, KillTimeOut property [File Server Resource Manager], KillTimeOut property [File Server Resource Manager],IFsrmActionCommand interface, fs.ifsrmactioncommand_killtimeout, fsrm.ifsrmactioncommand_killtimeout, fsrm/IFsrmActionCommand::KillTimeOut, fsrm/IFsrmActionCommand::get_KillTimeOut, fsrm/IFsrmActionCommand::put_KillTimeOut, get_KillTimeOut
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
 - IFsrmActionCommand::get_KillTimeOut
 - fsrm/IFsrmActionCommand::get_KillTimeOut
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
 - IFsrmActionCommand.KillTimeOut
 - IFsrmActionCommand.get_KillTimeOut
 - IFsrmActionCommand.put_KillTimeOut
---

# IFsrmActionCommand::get_KillTimeOut


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets the number of minutes the server waits before terminating the process that is 
    running the executable program specified in the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioncommand-get_executablepath">ExecutablePath</a> property.

This property is read/write.

## -parameters

## -remarks

For FSRM to terminate the process, the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioncommand-get_monitorcommand">IFsrmActionCommand::MonitorCommand</a> 
    property must be set to <b>VARIANT_TRUE</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>
