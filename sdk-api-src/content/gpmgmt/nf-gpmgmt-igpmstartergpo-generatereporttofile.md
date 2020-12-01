---
UID: NF:gpmgmt.IGPMStarterGPO.GenerateReportToFile
title: IGPMStarterGPO::GenerateReportToFile (gpmgmt.h)
description: The GenerateReportToFile method gets the report for the GPO and saves it to a file at a specified path.
helpviewer_keywords: ["GenerateReportToFile","GenerateReportToFile method [GPMC]","GenerateReportToFile method [GPMC]","IGPMStarterGPO interface","IGPMStarterGPO interface [GPMC]","GenerateReportToFile method","IGPMStarterGPO.GenerateReportToFile","IGPMStarterGPO::GenerateReportToFile","gpmc.igpmstartergpo_generatereporttofile","gpmgmt/IGPMStarterGPO::GenerateReportToFile"]
old-location: gpmc\igpmstartergpo_generatereporttofile.htm
tech.root: gpmc
ms.assetid: 29302091-0f2d-4511-a25b-9af078795d1d
ms.date: 12/05/2018
ms.keywords: GenerateReportToFile, GenerateReportToFile method [GPMC], GenerateReportToFile method [GPMC],IGPMStarterGPO interface, IGPMStarterGPO interface [GPMC],GenerateReportToFile method, IGPMStarterGPO.GenerateReportToFile, IGPMStarterGPO::GenerateReportToFile, gpmc.igpmstartergpo_generatereporttofile, gpmgmt/IGPMStarterGPO::GenerateReportToFile
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
 - IGPMStarterGPO::GenerateReportToFile
 - gpmgmt/IGPMStarterGPO::GenerateReportToFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gpmgmt.dll
api_name:
 - IGPMStarterGPO.GenerateReportToFile
---

# IGPMStarterGPO::GenerateReportToFile


## -description

The <b>GenerateReportToFile</b> method gets the report for the GPO and saves it to a file at a specified path.

## -parameters

### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.

### -param bstrTargetFilePath [in]

Binary string that contains the path to the file where the report is being saved. Use null-terminated string.

### -param ppIGPMResult [out]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface. The <b>Status</b> property contains a reference to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property of the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface is indeterminate and should not be relied upon.</div>
<div> </div>

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">IGPMStarterGPO</a>