---
UID: NF:fsrm.IFsrmActionEmail2.get_AttachmentFileListSize
title: IFsrmActionEmail2::get_AttachmentFileListSize (fsrm.h)
description: The maximum number of files to include in the list. (Get)
helpviewer_keywords: ["AttachmentFileListSize property [File Server Resource Manager]","AttachmentFileListSize property [File Server Resource Manager]","IFsrmActionEmail2 interface","IFsrmActionEmail2 interface [File Server Resource Manager]","AttachmentFileListSize property","IFsrmActionEmail2.AttachmentFileListSize","IFsrmActionEmail2.get_AttachmentFileListSize","IFsrmActionEmail2::AttachmentFileListSize","IFsrmActionEmail2::get_AttachmentFileListSize","IFsrmActionEmail2::put_AttachmentFileListSize","fs.ifsrmactionemail2_attachmentfilelistsize","fsrm.ifsrmactionemail2_attachmentfilelistsize","fsrm/IFsrmActionEmail2::AttachmentFileListSize","fsrm/IFsrmActionEmail2::get_AttachmentFileListSize","fsrm/IFsrmActionEmail2::put_AttachmentFileListSize","get_AttachmentFileListSize"]
old-location: fsrm\ifsrmactionemail2_attachmentfilelistsize.htm
tech.root: fsrm
ms.assetid: 355553d7-f237-481c-a6d4-51e0af2b3f5a
ms.date: 12/05/2018
ms.keywords: AttachmentFileListSize property [File Server Resource Manager], AttachmentFileListSize property [File Server Resource Manager],IFsrmActionEmail2 interface, IFsrmActionEmail2 interface [File Server Resource Manager],AttachmentFileListSize property, IFsrmActionEmail2.AttachmentFileListSize, IFsrmActionEmail2.get_AttachmentFileListSize, IFsrmActionEmail2::AttachmentFileListSize, IFsrmActionEmail2::get_AttachmentFileListSize, IFsrmActionEmail2::put_AttachmentFileListSize, fs.ifsrmactionemail2_attachmentfilelistsize, fsrm.ifsrmactionemail2_attachmentfilelistsize, fsrm/IFsrmActionEmail2::AttachmentFileListSize, fsrm/IFsrmActionEmail2::get_AttachmentFileListSize, fsrm/IFsrmActionEmail2::put_AttachmentFileListSize, get_AttachmentFileListSize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmActionEmail2::get_AttachmentFileListSize
 - fsrm/IFsrmActionEmail2::get_AttachmentFileListSize
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
 - IFsrmActionEmail2.AttachmentFileListSize
 - IFsrmActionEmail2.get_AttachmentFileListSize
 - IFsrmActionEmail2.put_AttachmentFileListSize
---

# IFsrmActionEmail2::get_AttachmentFileListSize


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

The maximum number of files to include in the list.

This property is read/write.

## -parameters

## -remarks

The attached file is a plain text file. The file contains a line for each file up to the maximum list size. 
    Each line is in the form, [Source File Path],[Source File Remote Paths].

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionemail2">IFsrmActionEmail2</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>
