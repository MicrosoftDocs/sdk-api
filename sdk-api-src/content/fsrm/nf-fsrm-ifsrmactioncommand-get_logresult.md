---
UID: NF:fsrm.IFsrmActionCommand.get_LogResult
title: IFsrmActionCommand::get_LogResult
author: windows-sdk-content
description: Retrieves or sets a value that determines whether FSRM logs an Application event that contains the return code of the executable program.
old-location: fsrm\ifsrmactioncommand_logresult.htm
tech.root: fsrm
ms.assetid: f05751e0-9cd9-4c12-8238-163b1e398b82
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmActionCommand interface [File Server Resource Manager],LogResult property, IFsrmActionCommand.LogResult, IFsrmActionCommand.get_LogResult, IFsrmActionCommand::LogResult, IFsrmActionCommand::get_LogResult, IFsrmActionCommand::put_LogResult, LogResult property [File Server Resource Manager], LogResult property [File Server Resource Manager],IFsrmActionCommand interface, fs.ifsrmactioncommand_logresult, fsrm.ifsrmactioncommand_logresult, fsrm/IFsrmActionCommand::LogResult, fsrm/IFsrmActionCommand::get_LogResult, fsrm/IFsrmActionCommand::put_LogResult, get_LogResult
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IFsrmActionCommand::get_LogResult


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets a value that determines whether FSRM logs an Application event that contains the 
    return code of the executable program.

This property is read/write.


## -parameters


## -remarks



For FSRM to log an event, the 
    <a href="https://msdn.microsoft.com/7aa420de-9be5-4333-a511-23e0443e633b">IFsrmActionCommand::MonitorCommand</a> 
    property must be set to <b>VARIANT_TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/b7f9fc8c-2f55-4a0e-879a-64c368abcabb">IFsrmActionCommand</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>



<a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>



<a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a>
 

 

