---
UID: NF:gpmgmt.IGPMRSOP.GenerateReport
title: IGPMRSOP::GenerateReport (gpmgmt.h)
description: The GenerateReport method generates a report on the RSoP data.
helpviewer_keywords: ["GenerateReport","GenerateReport method [GPMC]","GenerateReport method [GPMC]","IGPMRSOP interface","IGPMRSOP interface [GPMC]","GenerateReport method","IGPMRSOP.GenerateReport","IGPMRSOP::GenerateReport","gpmc.igpmrsop_generatereport","gpmgmt/IGPMRSOP::GenerateReport"]
old-location: gpmc\igpmrsop_generatereport.htm
tech.root: gpmc
ms.assetid: 86766a08-4f3a-4758-8abc-83db3408f0fd
ms.date: 12/05/2018
ms.keywords: GenerateReport, GenerateReport method [GPMC], GenerateReport method [GPMC],IGPMRSOP interface, IGPMRSOP interface [GPMC],GenerateReport method, IGPMRSOP.GenerateReport, IGPMRSOP::GenerateReport, gpmc.igpmrsop_generatereport, gpmgmt/IGPMRSOP::GenerateReport
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
 - IGPMRSOP::GenerateReport
 - gpmgmt/IGPMRSOP::GenerateReport
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
 - IGPMRSOP.GenerateReport
---

# IGPMRSOP::GenerateReport


## -description

The <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackup-generatereport">GenerateReport</a> method generates a report on the RSoP data.

## -parameters

### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.

### -param pvarGPMProgress [in, optional]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of report generation. If this parameter is not <b>NULL</b>, the call to <b>GenerateReport</b> is handled asynchronously. If this parameter is <b>NULL</b> the call to <b>GenerateReport</b> is handled synchronously and a pointer to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface is returned in <i>pvarGPMCancel</i>. This parameter must be <b>NULL</b> if the client should not receive asynchronous notifications.

### -param pvarGPMCancel [out, optional]

Receives a pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface that the client can use to cancel the report generation. This parameter is not returned when <i>pvarGPMProgress</i> is <b>NULL</b>.

### -param ppIGPMResult [out]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a>. The <b>Result</b> property contains  a binary string of XML or HTML. The <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmessage">Status</a> property contains a reference to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmrsop">IGPMRSOP</a>