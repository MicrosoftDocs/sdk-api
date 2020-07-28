---
UID: NF:gpmgmt.IGPMStarterGPOBackup.GenerateReportToFile
title: IGPMStarterGPOBackup::GenerateReportToFile (gpmgmt.h)
description: The GenerateReportToFile gets the report for the backup Starter GPO and saves it to a file at a specified path.
helpviewer_keywords: ["GenerateReportToFile","GenerateReportToFile method [GPMC]","GenerateReportToFile method [GPMC]","IGPMStarterGPOBackup interface","IGPMStarterGPOBackup interface [GPMC]","GenerateReportToFile method","IGPMStarterGPOBackup.GenerateReportToFile","IGPMStarterGPOBackup::GenerateReportToFile","gpmc.igpmstartergpobackup_generatereporttofile","gpmgmt/IGPMStarterGPOBackup::GenerateReportToFile"]
old-location: gpmc\igpmstartergpobackup_generatereporttofile.htm
tech.root: gpmc
ms.assetid: d7d05436-acd7-4b80-93e4-ea80e3eb1fff
ms.date: 12/05/2018
ms.keywords: GenerateReportToFile, GenerateReportToFile method [GPMC], GenerateReportToFile method [GPMC],IGPMStarterGPOBackup interface, IGPMStarterGPOBackup interface [GPMC],GenerateReportToFile method, IGPMStarterGPOBackup.GenerateReportToFile, IGPMStarterGPOBackup::GenerateReportToFile, gpmc.igpmstartergpobackup_generatereporttofile, gpmgmt/IGPMStarterGPOBackup::GenerateReportToFile
f1_keywords:
- gpmgmt/IGPMStarterGPOBackup.GenerateReportToFile
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gpmgmt.dll
api_name:
- IGPMStarterGPOBackup.GenerateReportToFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMStarterGPOBackup::GenerateReportToFile


## -description


The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackup-generatereporttofile">GenerateReportToFile</a> gets the report for the backup Starter GPO and saves it to a file at a specified path.


## -parameters




### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.


### -param bstrTargetFilePath [in]

Binary string that contains the path to the file where the report is being saved. Use null-terminated string.


### -param ppIGPMResult [out]

Pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface. The <b>Status</b> property contains a reference to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property is indeterminate and should not be relied upon.</div>
<div> </div>

#### - TargetFile [in]

Binary string that contains the path to the file where the report is being saved.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property is indeterminate and should not be relied upon.</div>
<div> </div>
<h3>VB</h3>
Returns a reference to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property is indeterminate and should not be relied upon.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdirex">IGPMBackupDirEx</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackup">IGPMStarterGPOBackup</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackupcollection">IGPMStarterGPOBackupCollection</a>
 

 

