---
UID: NF:fsrm.IFsrmSetting.put_SmtpServer
title: IFsrmSetting::put_SmtpServer
author: windows-sdk-content
description: Retrieves or sets the SMTP server that FSRM uses to send email.
old-location: fsrm\ifsrmsetting_smtpserver.htm
old-project: fsrm
ms.assetid: 3d16e478-6e53-44d4-85ca-a4c508d138de
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: FsrmSetting class [File Server Resource Manager],SmtpServer property, IFsrmSetting interface [File Server Resource Manager],SmtpServer property, IFsrmSetting.SmtpServer, IFsrmSetting.put_SmtpServer, IFsrmSetting::SmtpServer, IFsrmSetting::get_SmtpServer, IFsrmSetting::put_SmtpServer, SmtpServer property [File Server Resource Manager], SmtpServer property [File Server Resource Manager],FsrmSetting class, SmtpServer property [File Server Resource Manager],IFsrmSetting interface, fs.ifsrmsetting_smtpserver, fsrm.ifsrmsetting_smtpserver, fsrm/IFsrmSetting::SmtpServer, fsrm/IFsrmSetting::get_SmtpServer, fsrm/IFsrmSetting::put_SmtpServer, put_SmtpServer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IFsrmSetting.SmtpServer
 - IFsrmSetting.get_SmtpServer
 - IFsrmSetting.put_SmtpServer
 - FsrmSetting.SmtpServer
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmSetting::put_SmtpServer


## -description


Retrieves or sets the SMTP server that FSRM uses to send email.

This property is read/write.


## -parameters


## -remarks



This property must be set in order for FSRM to send email. To verify settings, call the 
    <a href="https://msdn.microsoft.com/dda57309-8e77-4934-bb3e-d208d4607ea5">IFsrmSetting::EmailTest</a> method.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/dda57309-8e77-4934-bb3e-d208d4607ea5">IFsrmSetting::EmailTest</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c27393a-9a84-4147-a7e0-582c0bf2d918">FsrmSetting</a>



<a href="https://msdn.microsoft.com/432fbaaa-7ddb-4d8c-bfbe-40cd26b08f9b">IFsrmSetting</a>
 

 

