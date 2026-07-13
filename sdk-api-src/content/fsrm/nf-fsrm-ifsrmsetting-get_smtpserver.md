---
UID: NF:fsrm.IFsrmSetting.get_SmtpServer
title: IFsrmSetting::get_SmtpServer (fsrm.h)
description: Retrieves or sets the SMTP server that FSRM uses to send email. (Get)
helpviewer_keywords: ["FsrmSetting class [File Server Resource Manager]","SmtpServer property","IFsrmSetting interface [File Server Resource Manager]","SmtpServer property","IFsrmSetting.SmtpServer","IFsrmSetting.get_SmtpServer","IFsrmSetting::SmtpServer","IFsrmSetting::get_SmtpServer","IFsrmSetting::put_SmtpServer","SmtpServer property [File Server Resource Manager]","SmtpServer property [File Server Resource Manager]","FsrmSetting class","SmtpServer property [File Server Resource Manager]","IFsrmSetting interface","fs.ifsrmsetting_smtpserver","fsrm.ifsrmsetting_smtpserver","fsrm/IFsrmSetting::SmtpServer","fsrm/IFsrmSetting::get_SmtpServer","fsrm/IFsrmSetting::put_SmtpServer","get_SmtpServer"]
old-location: fsrm\ifsrmsetting_smtpserver.htm
tech.root: fsrm
ms.assetid: 3d16e478-6e53-44d4-85ca-a4c508d138de
ms.date: 12/05/2018
ms.keywords: FsrmSetting class [File Server Resource Manager],SmtpServer property, IFsrmSetting interface [File Server Resource Manager],SmtpServer property, IFsrmSetting.SmtpServer, IFsrmSetting.get_SmtpServer, IFsrmSetting::SmtpServer, IFsrmSetting::get_SmtpServer, IFsrmSetting::put_SmtpServer, SmtpServer property [File Server Resource Manager], SmtpServer property [File Server Resource Manager],FsrmSetting class, SmtpServer property [File Server Resource Manager],IFsrmSetting interface, fs.ifsrmsetting_smtpserver, fsrm.ifsrmsetting_smtpserver, fsrm/IFsrmSetting::SmtpServer, fsrm/IFsrmSetting::get_SmtpServer, fsrm/IFsrmSetting::put_SmtpServer, get_SmtpServer
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
 - IFsrmSetting::get_SmtpServer
 - fsrm/IFsrmSetting::get_SmtpServer
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
 - IFsrmSetting.SmtpServer
 - IFsrmSetting.get_SmtpServer
 - IFsrmSetting.put_SmtpServer
 - FsrmSetting.SmtpServer
---

# IFsrmSetting::get_SmtpServer


## -description

Retrieves or sets the SMTP server that FSRM uses to send email.

This property is read/write.

## -parameters

## -remarks

This property must be set in order for FSRM to send email. To verify settings, call the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-emailtest">IFsrmSetting::EmailTest</a> method.


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmsetting-emailtest">IFsrmSetting::EmailTest</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmsetting">FsrmSetting</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmsetting">IFsrmSetting</a>
