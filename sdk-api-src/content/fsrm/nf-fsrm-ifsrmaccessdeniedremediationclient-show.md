---
UID: NF:fsrm.IFsrmAccessDeniedRemediationClient.Show
title: IFsrmAccessDeniedRemediationClient::Show (fsrm.h)
description: Displays the Access Denied Remediation (ADR) client dialog.
helpviewer_keywords: ["IFsrmAccessDeniedRemediationClient interface [File Server Resource Manager]","Show method","IFsrmAccessDeniedRemediationClient.Show","IFsrmAccessDeniedRemediationClient::Show","Show","Show method [File Server Resource Manager]","Show method [File Server Resource Manager]","IFsrmAccessDeniedRemediationClient interface","fs.ifsrmaccessdeniedremediationclient_show","fsrm.ifsrmaccessdeniedremediationclient_show","fsrm/IFsrmAccessDeniedRemediationClient::Show"]
old-location: fsrm\ifsrmaccessdeniedremediationclient_show.htm
tech.root: fsrm
ms.assetid: befebb2a-99a1-4a32-8bde-3b263d1f4459
ms.date: 12/05/2018
ms.keywords: IFsrmAccessDeniedRemediationClient interface [File Server Resource Manager],Show method, IFsrmAccessDeniedRemediationClient.Show, IFsrmAccessDeniedRemediationClient::Show, Show, Show method [File Server Resource Manager], Show method [File Server Resource Manager],IFsrmAccessDeniedRemediationClient interface, fs.ifsrmaccessdeniedremediationclient_show, fsrm.ifsrmaccessdeniedremediationclient_show, fsrm/IFsrmAccessDeniedRemediationClient::Show
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
 - IFsrmAccessDeniedRemediationClient::Show
 - fsrm/IFsrmAccessDeniedRemediationClient::Show
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
 - IFsrmAccessDeniedRemediationClient.Show
---

# IFsrmAccessDeniedRemediationClient::Show


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmadr">MSFT_FSRMAdr</a> and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmadrsettings">MSFT_FSRMADRSettings</a> classes.]

Displays the Access Denied Remediation (ADR) client dialog.

This method was introduced for applications that are already using the FSRM interfaces. Where possible it is 
    recommended to use the <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmadr">MSFT_FSRMAdr</a> and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmadrsettings">MSFT_FSRMADRSettings</a> WMI classes instead.

## -parameters

### -param parentWnd [in]

Handle to the window that will be the parent of the dialog that will be displayed.

### -param accessPath [in]

Path of the file being accessed.

### -param errorType [in]

The client error type as enumerated by the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-adrclienterrortype">AdrClientErrorType</a> enumeration.

### -param flags [in]

Reserved. Set to 0.

### -param windowTitle [in]

Optional text to display as the title of the dialog window that is opened.

### -param windowMessage [in]

Optional text to display above the instructions in the dialog window that is opened.

### -param result [out, retval]

Address of a value that will receive a <b>HRESULT</b> containing the result of the 
      operation.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaccessdeniedremediationclient">IFsrmAccessDeniedRemediationClient</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmadrsettings">MSFT_FSRMADRSettings</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmadr">MSFT_FSRMAdr</a>