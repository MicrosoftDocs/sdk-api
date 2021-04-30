---
UID: NF:gpmgmt.IGPMRSOP.GenerateReportToFile
title: IGPMRSOP::GenerateReportToFile (gpmgmt.h)
description: The GenerateReportToFile method generates a report on the RSoP data and saves it to a file at a specified path.
helpviewer_keywords: ["GenerateReportToFile","GenerateReportToFile method [GPMC]","GenerateReportToFile method [GPMC]","IGPMRSOP interface","IGPMRSOP interface [GPMC]","GenerateReportToFile method","IGPMRSOP.GenerateReportToFile","IGPMRSOP::GenerateReportToFile","gpmc.igpmrsop_generatereporttofile","gpmgmt/IGPMRSOP::GenerateReportToFile"]
old-location: gpmc\igpmrsop_generatereporttofile.htm
tech.root: gpmc
ms.assetid: 92a199d6-244f-44e5-8158-d77b8488fde0
ms.date: 12/05/2018
ms.keywords: GenerateReportToFile, GenerateReportToFile method [GPMC], GenerateReportToFile method [GPMC],IGPMRSOP interface, IGPMRSOP interface [GPMC],GenerateReportToFile method, IGPMRSOP.GenerateReportToFile, IGPMRSOP::GenerateReportToFile, gpmc.igpmrsop_generatereporttofile, gpmgmt/IGPMRSOP::GenerateReportToFile
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
 - IGPMRSOP::GenerateReportToFile
 - gpmgmt/IGPMRSOP::GenerateReportToFile
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
 - IGPMRSOP.GenerateReportToFile
---

## -description

The <b>GenerateReportToFile</b> method generates a report on the RSoP data and saves it to a file at a specified path.

## -parameters

### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.

### -param bstrTargetFilePath [in]

Binary string that contains the path to the file where the report is being saved. Use null-terminated string.

<div class="alert"><b>Note</b>  If the path to the file is not specified, then the report will be created in the "%windir%\system32\" directory.</div>
<div> </div>

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

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmrsop">IGPMRSOP</a>