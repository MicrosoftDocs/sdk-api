---
UID: NN:fsrm.IFsrmActionEventLog
title: IFsrmActionEventLog (fsrm.h)
description: Used to log an event to the Windows Application event log in response to a quota, file screen, or file management job event.
helpviewer_keywords: ["IFsrmActionEventLog","IFsrmActionEventLog interface [File Server Resource Manager]","IFsrmActionEventLog interface [File Server Resource Manager]","described","fs.ifsrmactioneventlog","fsrm.ifsrmactioneventlog","fsrm/IFsrmActionEventLog"]
old-location: fsrm\ifsrmactioneventlog.htm
tech.root: fsrm
ms.assetid: 418cd7aa-c363-4ab7-9c7e-2d0388483a8f
ms.date: 12/05/2018
ms.keywords: IFsrmActionEventLog, IFsrmActionEventLog interface [File Server Resource Manager], IFsrmActionEventLog interface [File Server Resource Manager],described, fs.ifsrmactioneventlog, fsrm.ifsrmactioneventlog, fsrm/IFsrmActionEventLog
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmActionEventLog
 - fsrm/IFsrmActionEventLog
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
 - IFsrmActionEventLog
---

# IFsrmActionEventLog interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Used to log an event to the Windows Application event log in response to a quota, file screen, or file 
    management job event.

To create an event log action, call one of the following methods and specify 
    <b>FsrmActionType_EventLog</b> as the action type:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-createnotificationaction">IFsrmFileManagementJob::CreateNotificationAction</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-createaction">IFsrmFileScreenBase::CreateAction</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-createthresholdaction">IFsrmQuotaBase::CreateThresholdAction</a>
</li>
</ul>The create methods return an <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a> interface. To get 
    this interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method 
    and specify <b>IID_IFsrmActionEventLog</b> as the interface identifier.

## -remarks

For most events, the event identifier is 12325. However, for events that a file management job logs, the event 
    identifier is 8244.

You must set the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactioneventlog-get_messagetext">MessageText</a> 
    property; the other property is optional.


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/fsrm/using-templates-to-define-quotas">Using Templates to Define Quotas</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionemail">IFsrmActionEmail</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionreport">IFsrmActionReport</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>