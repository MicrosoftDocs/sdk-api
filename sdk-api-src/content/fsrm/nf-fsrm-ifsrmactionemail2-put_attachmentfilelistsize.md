---
UID: NF:fsrm.IFsrmActionEmail2.put_AttachmentFileListSize
title: IFsrmActionEmail2::put_AttachmentFileListSize
author: windows-sdk-content
description: The maximum number of files to include in the list.
old-location: fsrm\ifsrmactionemail2_attachmentfilelistsize.htm
tech.root: fsrm
ms.assetid: 355553d7-f237-481c-a6d4-51e0af2b3f5a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AttachmentFileListSize property [File Server Resource Manager], AttachmentFileListSize property [File Server Resource Manager],IFsrmActionEmail2 interface, IFsrmActionEmail2 interface [File Server Resource Manager],AttachmentFileListSize property, IFsrmActionEmail2.AttachmentFileListSize, IFsrmActionEmail2.put_AttachmentFileListSize, IFsrmActionEmail2::AttachmentFileListSize, IFsrmActionEmail2::get_AttachmentFileListSize, IFsrmActionEmail2::put_AttachmentFileListSize, fs.ifsrmactionemail2_attachmentfilelistsize, fsrm.ifsrmactionemail2_attachmentfilelistsize, fsrm/IFsrmActionEmail2::AttachmentFileListSize, fsrm/IFsrmActionEmail2::get_AttachmentFileListSize, fsrm/IFsrmActionEmail2::put_AttachmentFileListSize, put_AttachmentFileListSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IFsrmActionEmail2.AttachmentFileListSize
 - IFsrmActionEmail2.get_AttachmentFileListSize
 - IFsrmActionEmail2.put_AttachmentFileListSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmActionEmail2::put_AttachmentFileListSize


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

The maximum number of files to include in the list.

This property is read/write.


## -parameters


## -remarks



The attached file is a plain text file. The file contains a line for each file up to the maximum list size. 
    Each line is in the form, [Source File Path],[Source File Remote Paths].




## -see-also




<a href="https://msdn.microsoft.com/278ef98d-fb1d-42a4-a740-07c5e713a230">IFsrmActionEmail2</a>



<a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>



<a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>



<a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a>
 

 

