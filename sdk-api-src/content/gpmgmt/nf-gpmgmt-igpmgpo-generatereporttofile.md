---
UID: NF:gpmgmt.IGPMGPO.GenerateReportToFile
title: IGPMGPO::GenerateReportToFile (gpmgmt.h)
description: Gets the report for a GPO and then saves the report to a file in a specified path.
helpviewer_keywords: ["GenerateReportToFile","GenerateReportToFile method [GPMC]","GenerateReportToFile method [GPMC]","IGPMGPO interface","IGPMGPO interface [GPMC]","GenerateReportToFile method","IGPMGPO.GenerateReportToFile","IGPMGPO::GenerateReportToFile","gpmc.igpmgpo_generatereporttofile","gpmgmt/IGPMGPO::GenerateReportToFile"]
old-location: gpmc\igpmgpo_generatereporttofile.htm
tech.root: gpmc
ms.assetid: 686b1461-3136-4351-adc4-32d558d62246
ms.date: 12/05/2018
ms.keywords: GenerateReportToFile, GenerateReportToFile method [GPMC], GenerateReportToFile method [GPMC],IGPMGPO interface, IGPMGPO interface [GPMC],GenerateReportToFile method, IGPMGPO.GenerateReportToFile, IGPMGPO::GenerateReportToFile, gpmc.igpmgpo_generatereporttofile, gpmgmt/IGPMGPO::GenerateReportToFile
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
 - IGPMGPO::GenerateReportToFile
 - gpmgmt/IGPMGPO::GenerateReportToFile
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
 - IGPMGPO.GenerateReportToFile
---

## -description

Gets the report for a GPO and then saves the report to a file in a specified path.

## -parameters

### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.

### -param bstrTargetFilePath [in]

Binary string that contains the path of the file in which the report is being saved. Use a null-terminated string.

### -param ppIGPMResult [out]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface. The <b>Status</b> property contains a reference to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property of the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface is indeterminate and should not be relied upon.</div>
<div> </div>

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property is indeterminate and should not be relied upon.</div>
<div> </div>
<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property is indeterminate and should not be relied upon.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>