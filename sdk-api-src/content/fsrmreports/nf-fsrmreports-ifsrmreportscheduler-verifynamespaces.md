---
UID: NF:fsrmreports.IFsrmReportScheduler.VerifyNamespaces
title: IFsrmReportScheduler::VerifyNamespaces (fsrmreports.h)
description: Verifies that the specified local directory paths that are used as the source for the reports are valid.
helpviewer_keywords: ["FsrmReportScheduler class [File Server Resource Manager]","VerifyNamespaces method","IFsrmReportScheduler interface [File Server Resource Manager]","VerifyNamespaces method","IFsrmReportScheduler.VerifyNamespaces","IFsrmReportScheduler::VerifyNamespaces","VerifyNamespaces","VerifyNamespaces method [File Server Resource Manager]","VerifyNamespaces method [File Server Resource Manager]","FsrmReportScheduler class","VerifyNamespaces method [File Server Resource Manager]","IFsrmReportScheduler interface","fs.ifsrmreportscheduler_verifynamespaces","fsrm.ifsrmreportscheduler_verifynamespaces","fsrmreports/IFsrmReportScheduler::VerifyNamespaces"]
old-location: fsrm\ifsrmreportscheduler_verifynamespaces.htm
tech.root: fsrm
ms.assetid: bb5139c8-e01f-48cf-a8a9-d3a3e5b86238
ms.date: 12/05/2018
ms.keywords: FsrmReportScheduler class [File Server Resource Manager],VerifyNamespaces method, IFsrmReportScheduler interface [File Server Resource Manager],VerifyNamespaces method, IFsrmReportScheduler.VerifyNamespaces, IFsrmReportScheduler::VerifyNamespaces, VerifyNamespaces, VerifyNamespaces method [File Server Resource Manager], VerifyNamespaces method [File Server Resource Manager],FsrmReportScheduler class, VerifyNamespaces method [File Server Resource Manager],IFsrmReportScheduler interface, fs.ifsrmreportscheduler_verifynamespaces, fsrm.ifsrmreportscheduler_verifynamespaces, fsrmreports/IFsrmReportScheduler::VerifyNamespaces
req.header: fsrmreports.h
req.include-header: FsrmReports.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmReports.idl
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
 - IFsrmReportScheduler::VerifyNamespaces
 - fsrmreports/IFsrmReportScheduler::VerifyNamespaces
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
 - IFsrmReportScheduler.VerifyNamespaces
 - FsrmReportScheduler.VerifyNamespaces
---

# IFsrmReportScheduler::VerifyNamespaces


## -description

<p class="CCE_Message">[Starting with Windows Server 2012 this method is not supported; use the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmscheduledtask">MSFT_FSRMScheduledTask</a> WMI class to manage 
    scheduled tasks.]

Verifies that the specified local directory paths that are used as the source for the reports are 
    valid.

## -parameters

### -param namespacesSafeArray [in]

A <b>VARIANT</b> that contains a <b>SAFEARRAY</b> of local 
      directory paths. Each element of the array is a variant of type <b>VT_BSTR</b>. Use the 
      <b>bstrVal</b> member of the variant to set the path.

## -returns

The method returns the following return values.

## -remarks

If the paths are valid, you can use them when calling the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportscheduler-createscheduletask">IFsrmReportScheduler::CreateScheduleTask</a> 
    method.

The paths are valid if:

<ul>
<li>All paths in the array are on NTFS volumes.</li>
<li>All paths in the array are on volumes that are online accessible.</li>
<li>For clusters, all paths are on volumes that are in the same failover group.</li>
</ul>
If one of the paths fails to validate, there is no indication of which path failed. To determine which path 
    failed, you need to call this method for each path separately. For clusters, if all paths validate, you need to 
    verify the cluster groups using the cluster APIs.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmreportscheduler">FsrmReportScheduler</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportscheduler">IFsrmReportScheduler</a>