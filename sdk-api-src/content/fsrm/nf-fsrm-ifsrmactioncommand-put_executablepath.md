---
UID: NF:fsrm.IFsrmActionCommand.put_ExecutablePath
title: IFsrmActionCommand::put_ExecutablePath
author: windows-sdk-content
description: Retrieves or sets the full path to the executable program or script to run.
old-location: fsrm\ifsrmactioncommand_executablepath.htm
old-project: fsrm
ms.assetid: c15b09e3-a8b6-4c73-82d7-8de7c2635f77
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: ExecutablePath property [File Server Resource Manager], ExecutablePath property [File Server Resource Manager],IFsrmActionCommand interface, IFsrmActionCommand interface [File Server Resource Manager],ExecutablePath property, IFsrmActionCommand.ExecutablePath, IFsrmActionCommand.put_ExecutablePath, IFsrmActionCommand::ExecutablePath, IFsrmActionCommand::get_ExecutablePath, IFsrmActionCommand::put_ExecutablePath, fs.ifsrmactioncommand_executablepath, fsrm.ifsrmactioncommand_executablepath, fsrm/IFsrmActionCommand::ExecutablePath, fsrm/IFsrmActionCommand::get_ExecutablePath, fsrm/IFsrmActionCommand::put_ExecutablePath, put_ExecutablePath
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmActionCommand::put_ExecutablePath


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
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




<a href="https://msdn.microsoft.com/b7f9fc8c-2f55-4a0e-879a-64c368abcabb">IFsrmActionCommand</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>



<a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>



<a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a>
 

 

