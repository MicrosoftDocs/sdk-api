---
UID: NN:fsrm.IFsrmActionReport
title: IFsrmActionReport (fsrm.h)
description: Used to generate a report in response to a quota or file screen event.
helpviewer_keywords: ["IFsrmActionReport","IFsrmActionReport interface [File Server Resource Manager]","IFsrmActionReport interface [File Server Resource Manager]","described","fs.ifsrmactionreport","fsrm.ifsrmactionreport","fsrm/IFsrmActionReport"]
old-location: fsrm\ifsrmactionreport.htm
tech.root: fsrm
ms.assetid: efff4cec-6985-40aa-a74e-bb2afdeb2a0a
ms.date: 12/05/2018
ms.keywords: IFsrmActionReport, IFsrmActionReport interface [File Server Resource Manager], IFsrmActionReport interface [File Server Resource Manager],described, fs.ifsrmactionreport, fsrm.ifsrmactionreport, fsrm/IFsrmActionReport
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
 - IFsrmActionReport
 - fsrm/IFsrmActionReport
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
 - IFsrmActionReport
---

# IFsrmActionReport interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Used to generate a report in response to a quota or file screen event.

To create a report action, call one of the following methods and specify 
    <b>FsrmActionType_Report</b> as the action type:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-createaction">IFsrmFileScreenBase::CreateAction</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-createthresholdaction">IFsrmQuotaBase::CreateThresholdAction</a>
</li>
</ul>The create methods return an <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a> interface. To get 
    this interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method 
    and specify <b>IID_IFsrmActionReport</b> as the interface identifier.

## -remarks

You must set the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmactionreport-get_reporttypes">ReportTypes</a> property; 
    the other property is optional.


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/updating-a-quota">Updating a Quota</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionemail">IFsrmActionEmail</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioneventlog">IFsrmActionEventLog</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>