---
UID: NN:fsrm.IFsrmActionEmail
title: IFsrmActionEmail
author: windows-sdk-content
description: Used to send an email message in response to a quota or file screen event.
old-location: fsrm\ifsrmactionemail.htm
tech.root: Fsrm
ms.assetid: 6eb6d82e-018d-4977-ad60-fce296c16e83
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFsrmActionEmail, IFsrmActionEmail interface [File Server Resource Manager], IFsrmActionEmail interface [File Server Resource Manager],described, fs.ifsrmactionemail, fsrm.ifsrmactionemail, fsrm/IFsrmActionEmail
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFsrmActionEmail
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmActionEmail interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Used to send an email message in response to a quota or file screen event.

To create an email action, call one of the following methods and specify 
    <b>FsrmActionType_Email</b> as the action type:
<ul>
<li>
<a href="https://msdn.microsoft.com/1d627e07-fa8c-4c22-acba-c08767b8ebaa">IFsrmFileScreenBase::CreateAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/27813041-ee42-4412-982e-fce594c5e648">IFsrmQuotaBase::CreateThresholdAction</a>
</li>
</ul>The create methods return an <a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a> interface. To get 
    this interface, call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method 
    and specify <b>IID_IFsrmActionEmail</b> as the interface identifier.

For file management jobs, see the <a href="https://msdn.microsoft.com/278ef98d-fb1d-42a4-a740-07c5e713a230">IFsrmActionEmail2</a> 
    interface.


## -remarks



You must set the <a href="https://msdn.microsoft.com/b440bae5-0e46-432b-992b-0de7dee16b12">MailTo</a> and 
    <a href="https://msdn.microsoft.com/5d4aef81-2be3-41c6-8639-8a0c5402615a">MessageText</a> properties; the other 
    properties are optional.




## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a>



<a href="https://msdn.microsoft.com/b7f9fc8c-2f55-4a0e-879a-64c368abcabb">IFsrmActionCommand</a>



<a href="https://msdn.microsoft.com/418cd7aa-c363-4ab7-9c7e-2d0388483a8f">IFsrmActionEventLog</a>



<a href="https://msdn.microsoft.com/efff4cec-6985-40aa-a74e-bb2afdeb2a0a">IFsrmActionReport</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>



<a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>



<a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a>
 

 

