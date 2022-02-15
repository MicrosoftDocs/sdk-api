---
UID: NN:fsrm.IFsrmAction
title: IFsrmAction (fsrm.h)
description: The base class for all FSRM action interfaces.
helpviewer_keywords: ["IFsrmAction","IFsrmAction interface [File Server Resource Manager]","IFsrmAction interface [File Server Resource Manager]","described","fs.ifsrmaction","fsrm.ifsrmaction","fsrm/IFsrmAction"]
old-location: fsrm\ifsrmaction.htm
tech.root: fsrm
ms.assetid: 81bfae1d-7d09-4ddc-9669-1da40dc72fd4
ms.date: 12/05/2018
ms.keywords: IFsrmAction, IFsrmAction interface [File Server Resource Manager], IFsrmAction interface [File Server Resource Manager],described, fs.ifsrmaction, fsrm.ifsrmaction, fsrm/IFsrmAction
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
 - IFsrmAction
 - fsrm/IFsrmAction
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
 - IFsrmAction
---

# IFsrmAction interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

The base class for all FSRM action interfaces.

To create an action, call one of the following methods:
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
</ul>Then, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
    returned interface for an interface of the specific action type. For an example, see 
    <a href="/previous-versions/windows/desktop/fsrm/performing-actions-based-on-file-screen-violations">Performing Actions Based on File Screen Violations</a>.

The following methods return a collection of actions:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-enumnotificationactions">IFsrmFileManagementJob::EnumNotificationActions</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-enumactions">IFsrmFileScreenBase::EnumActions</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-enumthresholdactions">IFsrmQuotaBase::EnumThresholdActions</a>
</li>
</ul>To get this interface from an item of the collection, call the 
    <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on the 
    <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface contained in the 
    <b>pdispVal</b> member of the variant.

Use the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmaction-get_actiontype">ActionType</a> property to determine the 
    type of action that this interface defines. You can then call the 
    <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on this interface to get an 
    interface that defines the action type. The See Also section lists the possible interfaces.

## -inheritance

The <b>IFsrmAction</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmAction</b> also has these types of members:

## -remarks

The FSRM server starts the action in response to quota or file screen event (for example, a directory size 
    exceeds a directory quota threshold or detection of a restricted file).

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionemail">IFsrmActionEmail</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionemail2">IFsrmActionEmail2</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioneventlog">IFsrmActionEventLog</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactionreport">IFsrmActionReport</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a>
