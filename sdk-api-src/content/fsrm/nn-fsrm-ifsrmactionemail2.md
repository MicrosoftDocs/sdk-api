---
UID: NN:fsrm.IFsrmActionEmail2
title: IFsrmActionEmail2
author: windows-sdk-content
description: Used to limit the number of expired files listed in the email notification.
old-location: fsrm\ifsrmactionemail2.htm
old-project: fsrm
ms.assetid: 278ef98d-fb1d-42a4-a740-07c5e713a230
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IFsrmActionEmail2, IFsrmActionEmail2 interface [File Server Resource Manager], IFsrmActionEmail2 interface [File Server Resource Manager],described, fs.ifsrmactionemail2, fsrm.ifsrmactionemail2, fsrm/IFsrmActionEmail2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - IFsrmActionEmail2
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmActionEmail2 interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Used to limit the number of expired files listed in the email notification.

Use this version of the interface for file management  notifications. To create an email action for file 
    management notifications, call the 
    <a href="https://msdn.microsoft.com/d0cb2ac1-842c-4ebb-adac-8298a0e0beed">IFsrmFileManagementJob::CreateNotificationAction</a> 
    method and specify <b>FsrmActionType_Email</b> as the action type.

The 
    <a href="https://msdn.microsoft.com/d0cb2ac1-842c-4ebb-adac-8298a0e0beed">CreateNotificationAction</a> 
    method returns an <a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a> interface. To get this interface, 
    call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method and specify 
    <b>IID_IFsrmActionEmail2</b> as the interface identifier.


## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/6eb6d82e-018d-4977-ad60-fce296c16e83">IFsrmActionEmail</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>



<a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>



<a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a>
 

 

