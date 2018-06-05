---
UID: NF:fsrm.IFsrmActionCommand.put_MonitorCommand
title: IFsrmActionCommand::put_MonitorCommand
author: windows-sdk-content
description: Retrieves or sets a value that determines whether FSRM will monitor the executable program specified in the ExecutablePath property.
old-location: fsrm\ifsrmactioncommand_monitorcommand.htm
old-project: Fsrm
ms.assetid: 7aa420de-9be5-4333-a511-23e0443e633b
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmActionCommand interface [File Server Resource Manager],MonitorCommand property, IFsrmActionCommand.MonitorCommand, IFsrmActionCommand.put_MonitorCommand, IFsrmActionCommand::MonitorCommand, IFsrmActionCommand::get_MonitorCommand, IFsrmActionCommand::put_MonitorCommand, MonitorCommand property [File Server Resource Manager], MonitorCommand property [File Server Resource Manager],IFsrmActionCommand interface, fs.ifsrmactioncommand_monitorcommand, fsrm.ifsrmactioncommand_monitorcommand, fsrm/IFsrmActionCommand::MonitorCommand, fsrm/IFsrmActionCommand::get_MonitorCommand, fsrm/IFsrmActionCommand::put_MonitorCommand, put_MonitorCommand
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmActionCommand.MonitorCommand
-	IFsrmActionCommand.get_MonitorCommand
-	IFsrmActionCommand.put_MonitorCommand
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmActionCommand::put_MonitorCommand


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Retrieves or sets a value that determines whether FSRM will monitor the executable program specified 
    in the <a href="https://msdn.microsoft.com/c15b09e3-a8b6-4c73-82d7-8de7c2635f77">ExecutablePath</a> 
    property.

This property is read/write.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/2873f1c4-6827-411f-b12f-9c282cf91119">KillTimeOut</a> and 
    <a href="https://msdn.microsoft.com/f05751e0-9cd9-4c12-8238-163b1e398b82">LogResult</a> properties are ignored if this 
    property is not set to <b>VARIANT_TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/b7f9fc8c-2f55-4a0e-879a-64c368abcabb">IFsrmActionCommand</a>



<a href="https://msdn.microsoft.com/f05751e0-9cd9-4c12-8238-163b1e398b82">IFsrmActionCommand::LogResult</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>



<a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>



<a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a>
 

 

