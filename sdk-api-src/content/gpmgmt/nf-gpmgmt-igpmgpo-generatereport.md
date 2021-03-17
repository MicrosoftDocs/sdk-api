---
UID: NF:gpmgmt.IGPMGPO.GenerateReport
title: IGPMGPO::GenerateReport (gpmgmt.h)
description: Gets the report for a GPO.
helpviewer_keywords: ["GenerateReport","GenerateReport method [GPMC]","GenerateReport method [GPMC]","IGPMGPO interface","IGPMGPO interface [GPMC]","GenerateReport method","IGPMGPO.GenerateReport","IGPMGPO::GenerateReport","gpmc.igpmgpo_generatereport","gpmgmt/IGPMGPO::GenerateReport"]
old-location: gpmc\igpmgpo_generatereport.htm
tech.root: gpmc
ms.assetid: 19b3b027-59f1-4c31-896b-5b5fd23b9be4
ms.date: 12/05/2018
ms.keywords: GenerateReport, GenerateReport method [GPMC], GenerateReport method [GPMC],IGPMGPO interface, IGPMGPO interface [GPMC],GenerateReport method, IGPMGPO.GenerateReport, IGPMGPO::GenerateReport, gpmc.igpmgpo_generatereport, gpmgmt/IGPMGPO::GenerateReport
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
 - IGPMGPO::GenerateReport
 - gpmgmt/IGPMGPO::GenerateReport
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
 - IGPMGPO.GenerateReport
---

# IGPMGPO::GenerateReport


## -description

Gets the report for a GPO.

## -parameters

### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.

### -param pvarGPMProgress [in, optional]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the copy operation. If not <b>NULL</b>, the call to <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackup-generatereport">GenerateReport</a> is handled asynchronously and <i>pvarGPMCancel</i> receives a pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface.   If this parameter is <b>NULL</b> the call to <b>GenerateReport</b> is handled synchronously. The <i>pvarGPMProgress</i> parameter must be <b>NULL</b> if the client should not receive asynchronous notifications.

### -param pvarGPMCancel [out, optional]

Receives a pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface that the client can use to cancel the copy operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.

### -param ppIGPMResult [out]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface. The <b>Result</b> property contains  a binary string of XML or HTML. The <b>Status</b> property contains a reference to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>