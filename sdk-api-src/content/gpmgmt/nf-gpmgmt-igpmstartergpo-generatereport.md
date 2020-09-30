---
UID: NF:gpmgmt.IGPMStarterGPO.GenerateReport
title: IGPMStarterGPO::GenerateReport (gpmgmt.h)
description: Gets the report for the Starter GPO.
helpviewer_keywords: ["GenerateReport","GenerateReport method [GPMC]","GenerateReport method [GPMC]","IGPMStarterGPO interface","IGPMStarterGPO interface [GPMC]","GenerateReport method","IGPMStarterGPO.GenerateReport","IGPMStarterGPO::GenerateReport","gpmc.igpmstartergpo_generatereport","gpmgmt/IGPMStarterGPO::GenerateReport"]
old-location: gpmc\igpmstartergpo_generatereport.htm
tech.root: gpmc
ms.assetid: 127cde40-abe0-42da-9845-2fe1c0b1f1f1
ms.date: 12/05/2018
ms.keywords: GenerateReport, GenerateReport method [GPMC], GenerateReport method [GPMC],IGPMStarterGPO interface, IGPMStarterGPO interface [GPMC],GenerateReport method, IGPMStarterGPO.GenerateReport, IGPMStarterGPO::GenerateReport, gpmc.igpmstartergpo_generatereport, gpmgmt/IGPMStarterGPO::GenerateReport
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
 - IGPMStarterGPO::GenerateReport
 - gpmgmt/IGPMStarterGPO::GenerateReport
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
 - IGPMStarterGPO.GenerateReport
---

# IGPMStarterGPO::GenerateReport


## -description

 Gets the report for the Starter GPO.

## -parameters

### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.

### -param pvarGPMProgress [in, optional]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the copy operation. If not <b>NULL</b>, the call to <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackup-generatereport">GenerateReport</a> is handled asynchronously and <i>pvarGPMCancel</i> receives a pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface.   If this parameter is <b>NULL</b> the call to <b>GenerateReport</b> is handled synchronously. The <i>pvarGPMProgress</i> parameter must be <b>NULL</b> if the client should not receive asynchronous notifications.

### -param pvarGPMCancel [in, optional]

Receives a pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface that the client can use to cancel the copy operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.

### -param ppIGPMResult [out]

Pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a>. The Result property contains  a binary string of XML or HTML. The Status property contains a reference to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">IGPMStarterGPO</a>