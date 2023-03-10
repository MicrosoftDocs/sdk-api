---
UID: NF:fsrm.IFsrmSetting.put_MailFrom
title: IFsrmSetting::put_MailFrom (fsrm.h)
description: Retrieves or sets the default email address from which email messages are sent. (Put)
helpviewer_keywords: ["FsrmSetting class [File Server Resource Manager]","MailFrom property","IFsrmSetting interface [File Server Resource Manager]","MailFrom property","IFsrmSetting.MailFrom","IFsrmSetting.put_MailFrom","IFsrmSetting::MailFrom","IFsrmSetting::get_MailFrom","IFsrmSetting::put_MailFrom","MailFrom property [File Server Resource Manager]","MailFrom property [File Server Resource Manager]","FsrmSetting class","MailFrom property [File Server Resource Manager]","IFsrmSetting interface","fs.ifsrmsetting_mailfrom","fsrm.ifsrmsetting_mailfrom","fsrm/IFsrmSetting::MailFrom","fsrm/IFsrmSetting::get_MailFrom","fsrm/IFsrmSetting::put_MailFrom","put_MailFrom"]
old-location: fsrm\ifsrmsetting_mailfrom.htm
tech.root: fsrm
ms.assetid: 62296c6c-d75b-4669-a665-a0c4321218b6
ms.date: 12/05/2018
ms.keywords: FsrmSetting class [File Server Resource Manager],MailFrom property, IFsrmSetting interface [File Server Resource Manager],MailFrom property, IFsrmSetting.MailFrom, IFsrmSetting.put_MailFrom, IFsrmSetting::MailFrom, IFsrmSetting::get_MailFrom, IFsrmSetting::put_MailFrom, MailFrom property [File Server Resource Manager], MailFrom property [File Server Resource Manager],FsrmSetting class, MailFrom property [File Server Resource Manager],IFsrmSetting interface, fs.ifsrmsetting_mailfrom, fsrm.ifsrmsetting_mailfrom, fsrm/IFsrmSetting::MailFrom, fsrm/IFsrmSetting::get_MailFrom, fsrm/IFsrmSetting::put_MailFrom, put_MailFrom
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h, FsrmTlb.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmSetting::put_MailFrom
 - fsrm/IFsrmSetting::put_MailFrom
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
 - IFsrmSetting.MailFrom
 - IFsrmSetting.get_MailFrom
 - IFsrmSetting.put_MailFrom
 - FsrmSetting.MailFrom
---

# IFsrmSetting::put_MailFrom


## -description

Retrieves or sets the default email address from which email messages are sent.

This property is read/write.

## -parameters

## -remarks

The default is" FSRM@<i>local machine name</i>". You cannot set this to 
    "[Admin Email]".


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmsetting">IFsrmSetting</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmsetting">FsrmSetting</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmsetting">IFsrmSetting</a>
