---
UID: NF:gpmgmt.IGPMBackup.GenerateReport
title: IGPMBackup::GenerateReport (gpmgmt.h)
description: Gets the report for the backup Group Policy object (GPO).
helpviewer_keywords: ["GPMBackup object [GPMC]","GenerateReport method","GenerateReport","GenerateReport method [GPMC]","GenerateReport method [GPMC]","GPMBackup object","GenerateReport method [GPMC]","IGPMBackup interface","IGPMBackup interface [GPMC]","GenerateReport method","IGPMBackup.GenerateReport","IGPMBackup::GenerateReport","gpmc.igpmbackup_generatereport","gpmgmt/IGPMBackup::GenerateReport"]
old-location: gpmc\igpmbackup_generatereport.htm
tech.root: gpmc
ms.assetid: d5daa512-547f-4b2d-85b3-0f6e9244acb2
ms.date: 12/05/2018
ms.keywords: GPMBackup object [GPMC],GenerateReport method, GenerateReport, GenerateReport method [GPMC], GenerateReport method [GPMC],GPMBackup object, GenerateReport method [GPMC],IGPMBackup interface, IGPMBackup interface [GPMC],GenerateReport method, IGPMBackup.GenerateReport, IGPMBackup::GenerateReport, gpmc.igpmbackup_generatereport, gpmgmt/IGPMBackup::GenerateReport
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
 - IGPMBackup::GenerateReport
 - gpmgmt/IGPMBackup::GenerateReport
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
 - IGPMBackup.GenerateReport
 - GPMBackup.GenerateReport
---

# IGPMBackup::GenerateReport


## -description

Gets the report for the backup Group Policy object (GPO).

## -parameters

### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.

### -param pvarGPMProgress [in, optional]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a> interface. If <i>pvarGPMProgress</i> is <b>NULL</b>, the call to <b>GenerateReport</b> is handled synchronously. If  not <b>NULL</b>, the call to <b>GenerateReport</b> is handled asynchronously, and <i>pvarGPMCancel</i> returns a pointer to    <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> .

### -param pvarGPMCancel [out, optional]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface. A value for this parameter is returned only when <i>pvarGPMProgress</i> is specified and is not <b>NULL</b>.

### -param ppIGPMResult [out]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface. The <b>Result</b> property contains  a string of XML or HTML. The <b>Status</b> property contains a reference to an  <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">IGPMBackupDir</a>