---
UID: NN:fsrm.IFsrmActionCommand
title: IFsrmActionCommand (fsrm.h)
author: windows-sdk-content
description: Used to run a command or script in response to a quota, file screen, or file management job event.
old-location: fsrm\ifsrmactioncommand.htm
tech.root: fsrm
ms.assetid: b7f9fc8c-2f55-4a0e-879a-64c368abcabb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmActionCommand, IFsrmActionCommand interface [File Server Resource Manager], IFsrmActionCommand interface [File Server Resource Manager],described, fs.ifsrmactioncommand, fsrm.ifsrmactioncommand, fsrm/IFsrmActionCommand
ms.topic: interface
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmActionCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmActionCommand interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Used to run a command or script in response to a quota, file screen, or file management job  
    event.

To create a command action, call one of the following methods and specify 
    <b>FsrmActionType_Command</b> as the action type:
<ul>
<li>
<a href="https://msdn.microsoft.com/d0cb2ac1-842c-4ebb-adac-8298a0e0beed">IFsrmFileManagementJob::CreateNotificationAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d627e07-fa8c-4c22-acba-c08767b8ebaa">IFsrmFileScreenBase::CreateAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/27813041-ee42-4412-982e-fce594c5e648">IFsrmQuotaBase::CreateThresholdAction</a>
</li>
</ul>The create methods return an <a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a> interface. To get 
    this interface, call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method 
    and specify <b>IID_IFsrmActionCommand</b> as the interface identifier.


## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a>



<a href="https://msdn.microsoft.com/6eb6d82e-018d-4977-ad60-fce296c16e83">IFsrmActionEmail</a>



<a href="https://msdn.microsoft.com/418cd7aa-c363-4ab7-9c7e-2d0388483a8f">IFsrmActionEventLog</a>



<a href="https://msdn.microsoft.com/efff4cec-6985-40aa-a74e-bb2afdeb2a0a">IFsrmActionReport</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>



<a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>



<a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a>
 

 

