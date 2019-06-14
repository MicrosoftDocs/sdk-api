---
UID: NF:fsrm.IFsrmActionCommand.put_LogResult
title: IFsrmActionCommand::put_LogResult (fsrm.h)
author: windows-sdk-content
description: Retrieves or sets a value that determines whether FSRM logs an Application event that contains the return code of the executable program.
old-location: fsrm\ifsrmactioncommand_logresult.htm
tech.root: fsrm
ms.assetid: f05751e0-9cd9-4c12-8238-163b1e398b82
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmActionCommand interface [File Server Resource Manager],LogResult property, IFsrmActionCommand.LogResult, IFsrmActionCommand.put_LogResult, IFsrmActionCommand::LogResult, IFsrmActionCommand::get_LogResult, IFsrmActionCommand::put_LogResult, LogResult property [File Server Resource Manager], LogResult property [File Server Resource Manager],IFsrmActionCommand interface, fs.ifsrmactioncommand_logresult, fsrm.ifsrmactioncommand_logresult, fsrm/IFsrmActionCommand::LogResult, fsrm/IFsrmActionCommand::get_LogResult, fsrm/IFsrmActionCommand::put_LogResult, put_LogResult
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmActionCommand.LogResult
 - IFsrmActionCommand.get_LogResult
 - IFsrmActionCommand.put_LogResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmActionCommand::put_LogResult


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets a value that determines whether FSRM logs an Application event that contains the 
    return code of the executable program.

This property is read/write.


## -parameters


## -remarks



For FSRM to log an event, the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioncommand-get_monitorcommand">IFsrmActionCommand::MonitorCommand</a> 
    property must be set to <b>VARIANT_TRUE</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>
 

 

