---
UID: NF:fsrm.IFsrmActionCommand.get_Account
title: IFsrmActionCommand::get_Account (fsrm.h)
description: Retrieves or sets the system account that is used to run the executable program specified in the ExecutablePath property. (Get)
helpviewer_keywords: ["Account property [File Server Resource Manager]","Account property [File Server Resource Manager]","IFsrmActionCommand interface","IFsrmActionCommand interface [File Server Resource Manager]","Account property","IFsrmActionCommand.Account","IFsrmActionCommand.get_Account","IFsrmActionCommand::Account","IFsrmActionCommand::get_Account","IFsrmActionCommand::put_Account","fs.ifsrmactioncommand_account","fsrm.ifsrmactioncommand_account","fsrm/IFsrmActionCommand::Account","fsrm/IFsrmActionCommand::get_Account","fsrm/IFsrmActionCommand::put_Account","get_Account"]
old-location: fsrm\ifsrmactioncommand_account.htm
tech.root: fsrm
ms.assetid: 24f0bf5c-064c-4f1e-b69f-23374ea78324
ms.date: 12/05/2018
ms.keywords: Account property [File Server Resource Manager], Account property [File Server Resource Manager],IFsrmActionCommand interface, IFsrmActionCommand interface [File Server Resource Manager],Account property, IFsrmActionCommand.Account, IFsrmActionCommand.get_Account, IFsrmActionCommand::Account, IFsrmActionCommand::get_Account, IFsrmActionCommand::put_Account, fs.ifsrmactioncommand_account, fsrm.ifsrmactioncommand_account, fsrm/IFsrmActionCommand::Account, fsrm/IFsrmActionCommand::get_Account, fsrm/IFsrmActionCommand::put_Account, get_Account
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
 - IFsrmActionCommand::get_Account
 - fsrm/IFsrmActionCommand::get_Account
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
 - IFsrmActionCommand.Account
 - IFsrmActionCommand.get_Account
 - IFsrmActionCommand.put_Account
---

# IFsrmActionCommand::get_Account


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets the system account that is used to run the executable program specified in the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioncommand-get_executablepath">ExecutablePath</a> property.

This property is read/write.

## -parameters

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>
