---
UID: NF:gpmgmt.IGPMStarterGPOBackup.GenerateReport
title: IGPMStarterGPOBackup::GenerateReport (gpmgmt.h)
description: The GenerateReport method gets the report for the backup GPO.
helpviewer_keywords: ["GenerateReport","GenerateReport method [GPMC]","GenerateReport method [GPMC]","IGPMStarterGPOBackup interface","IGPMStarterGPOBackup interface [GPMC]","GenerateReport method","IGPMStarterGPOBackup.GenerateReport","IGPMStarterGPOBackup::GenerateReport","gpmc.igpmstartergpobackup_generatereport","gpmgmt/IGPMStarterGPOBackup::GenerateReport"]
old-location: gpmc\igpmstartergpobackup_generatereport.htm
tech.root: gpmc
ms.assetid: ce0dd44f-dfd9-4e7c-9854-9decbc25ec54
ms.date: 12/05/2018
ms.keywords: GenerateReport, GenerateReport method [GPMC], GenerateReport method [GPMC],IGPMStarterGPOBackup interface, IGPMStarterGPOBackup interface [GPMC],GenerateReport method, IGPMStarterGPOBackup.GenerateReport, IGPMStarterGPOBackup::GenerateReport, gpmc.igpmstartergpobackup_generatereport, gpmgmt/IGPMStarterGPOBackup::GenerateReport
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMStarterGPOBackup::GenerateReport
 - gpmgmt/IGPMStarterGPOBackup::GenerateReport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMStarterGPOBackup.GenerateReport
---

# IGPMStarterGPOBackup::GenerateReport


## -description

The <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackup-generatereport">GenerateReport</a> method gets the report for the backup GPO.

## -parameters

### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.

### -param pvarGPMProgress [in, optional]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a> interface. If <i>pvarGPMProgress</i> is null, the call to <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackup-generatereport">GenerateReport</a> is handled synchronously. If  not null, the call to <b>GenerateReport</b> is handled asynchronously and <i>pvarGPMCancel</i> returns a pointer to   <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a>.

### -param pvarGPMCancel [out, optional]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface. A value for this parameter is returned only when <i>pvarGPMProgress</i> is specified and is not null.

### -param ppIGPMResult [out]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a>. The Result property contains  a string of XML or HTML. The Status property contains a reference to an  <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdirex">IGPMBackupDirEx</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackup">IGPMStarterGPOBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackupcollection">IGPMStarterGPOBackupCollection</a>