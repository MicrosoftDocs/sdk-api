---
UID: NF:fsrm.IFsrmActionCommand.get_WorkingDirectory
title: IFsrmActionCommand::get_WorkingDirectory method
author: windows-driver-content
description: Retrieves or sets the working directory in which the executable program will run.
old-location: fsrm\ifsrmactioncommand_workingdirectory.htm
old-project: Fsrm
ms.assetid: 6844b6c3-11b4-4544-bd4e-bf2b89af00b7
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFsrmActionCommand, IFsrmActionCommand interface [File Server Resource Manager], WorkingDirectory property, IFsrmActionCommand.WorkingDirectory, IFsrmActionCommand::get_WorkingDirectory, IFsrmActionCommand::put_WorkingDirectory, WorkingDirectory property [File Server Resource Manager], WorkingDirectory property [File Server Resource Manager], IFsrmActionCommand interface, fs.ifsrmactioncommand_workingdirectory, fsrm.ifsrmactioncommand_workingdirectory, fsrm/IFsrmActionCommand::WorkingDirectory, fsrm/IFsrmActionCommand::get_WorkingDirectory, fsrm/IFsrmActionCommand::put_WorkingDirectory, get_WorkingDirectory,IFsrmActionCommand.get_WorkingDirectory
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
req.typenames: FILTERED_DATA_SOURCES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmActionCommand.WorkingDirectory
-	IFsrmActionCommand.get_WorkingDirectory
-	IFsrmActionCommand.put_WorkingDirectory
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmActionCommand::get_WorkingDirectory method


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets the working directory in which the executable program will run.

This property is read/write.


## -parameters


## -remarks



The path can contain environment variables.

The path must exist when you set the property or the command executes. If the path does not exist when the 
    command executes, FSRM writes an event to the Application log.




## -see-also




<a href="https://msdn.microsoft.com/b7f9fc8c-2f55-4a0e-879a-64c368abcabb">IFsrmActionCommand</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>



<a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>



<a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a>
 

 

