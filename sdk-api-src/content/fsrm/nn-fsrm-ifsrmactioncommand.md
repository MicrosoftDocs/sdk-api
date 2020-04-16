---
UID: NN:fsrm.IFsrmActionCommand
title: IFsrmActionCommand (fsrm.h)
description: Used to run a command or script in response to a quota, file screen, or file management job event.helpviewer_keywords: ["IFsrmActionCommand","IFsrmActionCommand interface [File Server Resource Manager]","IFsrmActionCommand interface [File Server Resource Manager]","described","fs.ifsrmactioncommand","fsrm.ifsrmactioncommand","fsrm/IFsrmActionCommand"]
old-location: fsrm\ifsrmactioncommand.htm
tech.root: fsrm
ms.assetid: b7f9fc8c-2f55-4a0e-879a-64c368abcabb
ms.date: 12/05/2018
ms.keywords: IFsrmActionCommand, IFsrmActionCommand interface [File Server Resource Manager], IFsrmActionCommand interface [File Server Resource Manager],described, fs.ifsrmactioncommand, fsrm.ifsrmactioncommand, fsrm/IFsrmActionCommand
f1_keywords:
- fsrm/IFsrmActionCommand
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmActionCommand interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Used to run a command or script in response to a quota, file screen, or file management job  
    event.

To create a command action, call one of the following methods and specify 
    <b>FsrmActionType_Command</b> as the action type:
<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createnotificationaction">IFsrmFileManagementJob::CreateNotificationAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-createaction">IFsrmFileScreenBase::CreateAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-createthresholdaction">IFsrmQuotaBase::CreateThresholdAction</a>
</li>
</ul>The create methods return an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a> interface. To get 
    this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method 
    and specify <b>IID_IFsrmActionCommand</b> as the interface identifier.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionemail">IFsrmActionEmail</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioneventlog">IFsrmActionEventLog</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionreport">IFsrmActionReport</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>
 

 

