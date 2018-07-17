---
UID: NF:fsrm.IFsrmAccessDeniedRemediationClient.Show
title: IFsrmAccessDeniedRemediationClient::Show
author: windows-sdk-content
description: Displays the Access Denied Remediation (ADR) client dialog.
old-location: fsrm\ifsrmaccessdeniedremediationclient_show.htm
old-project: Fsrm
ms.assetid: befebb2a-99a1-4a32-8bde-3b263d1f4459
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IFsrmAccessDeniedRemediationClient interface [File Server Resource Manager],Show method, IFsrmAccessDeniedRemediationClient.Show, IFsrmAccessDeniedRemediationClient::Show, Show, Show method [File Server Resource Manager], Show method [File Server Resource Manager],IFsrmAccessDeniedRemediationClient interface, fs.ifsrmaccessdeniedremediationclient_show, fsrm.ifsrmaccessdeniedremediationclient_show, fsrm/IFsrmAccessDeniedRemediationClient::Show
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IFsrmAccessDeniedRemediationClient.Show
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmAccessDeniedRemediationClient::Show


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/fec0343f-4ab6-4b8c-b365-e510286af2be">MSFT_FSRMAdr</a> and 
    <a href="https://msdn.microsoft.com/0ddadb89-7059-43bb-9b8b-e31976ce715a">MSFT_FSRMADRSettings</a> classes.]

Displays the Access Denied Remediation (ADR) client dialog.

This method was introduced for applications that are already using the FSRM interfaces. Where possible it is 
    recommended to use the <a href="https://msdn.microsoft.com/fec0343f-4ab6-4b8c-b365-e510286af2be">MSFT_FSRMAdr</a> and 
    <a href="https://msdn.microsoft.com/0ddadb89-7059-43bb-9b8b-e31976ce715a">MSFT_FSRMADRSettings</a> WMI classes instead.


## -parameters




### -param parentWnd [in]

Handle to the window that will be the parent of the dialog that will be displayed.


### -param accessPath [in]

Path of the file being accessed.


### -param errorType [in]

The client error type as enumerated by the 
      <a href="https://msdn.microsoft.com/83e2c39b-ab3b-46c9-bb11-3f03f8193a7c">AdrClientErrorType</a> enumeration.


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/572d2985-a579-4bfa-a305-403b6be516ca">IFsrmAccessDeniedRemediationClient</a>



<a href="https://msdn.microsoft.com/0ddadb89-7059-43bb-9b8b-e31976ce715a">MSFT_FSRMADRSettings</a>



<a href="https://msdn.microsoft.com/fec0343f-4ab6-4b8c-b365-e510286af2be">MSFT_FSRMAdr</a>
 

 

