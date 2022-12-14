---
UID: NN:fsrm.IFsrmAccessDeniedRemediationClient
title: IFsrmAccessDeniedRemediationClient (fsrm.h)
description: Used to show the Access Denied Remediation (ADR) client user interface.
helpviewer_keywords: ["IFsrmAccessDeniedRemediationClient","IFsrmAccessDeniedRemediationClient interface [File Server Resource Manager]","IFsrmAccessDeniedRemediationClient interface [File Server Resource Manager]","described","fs.ifsrmaccessdeniedremediationclient","fsrm.ifsrmaccessdeniedremediationclient","fsrm/IFsrmAccessDeniedRemediationClient"]
old-location: fsrm\ifsrmaccessdeniedremediationclient.htm
tech.root: fsrm
ms.assetid: 572d2985-a579-4bfa-a305-403b6be516ca
ms.date: 12/05/2018
ms.keywords: IFsrmAccessDeniedRemediationClient, IFsrmAccessDeniedRemediationClient interface [File Server Resource Manager], IFsrmAccessDeniedRemediationClient interface [File Server Resource Manager],described, fs.ifsrmaccessdeniedremediationclient, fsrm.ifsrmaccessdeniedremediationclient, fsrm/IFsrmAccessDeniedRemediationClient
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - IFsrmAccessDeniedRemediationClient
 - fsrm/IFsrmAccessDeniedRemediationClient
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
 - IFsrmAccessDeniedRemediationClient
---

# IFsrmAccessDeniedRemediationClient interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmadr">MSFT_FSRMAdr</a> and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmadrsettings">MSFT_FSRMADRSettings</a> classes.]

Used to show the Access Denied Remediation (ADR) client user interface.

This interface was introduced for applications that are already using the FSRM interfaces. Where possible it is 
    recommended to use the <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmadr">MSFT_FSRMAdr</a> and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmadrsettings">MSFT_FSRMADRSettings</a> WMI classes instead.

## -inheritance

The <b>IFsrmAccessDeniedRemediationClient</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmAccessDeniedRemediationClient</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmadrsettings">MSFT_FSRMADRSettings</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmadr">MSFT_FSRMAdr</a>
