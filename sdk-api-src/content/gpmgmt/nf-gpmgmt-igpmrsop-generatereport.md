---
UID: NF:gpmgmt.IGPMRSOP.GenerateReport
title: IGPMRSOP::GenerateReport
author: windows-sdk-content
description: The GenerateReport method generates a report on the RSoP data.
old-location: gpmc\igpmrsop_generatereport.htm
tech.root: gpmc
ms.assetid: 86766a08-4f3a-4758-8abc-83db3408f0fd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GenerateReport, GenerateReport method [GPMC], GenerateReport method [GPMC],IGPMRSOP interface, IGPMRSOP interface [GPMC],GenerateReport method, IGPMRSOP.GenerateReport, IGPMRSOP::GenerateReport, gpmc.igpmrsop_generatereport, gpmgmt/IGPMRSOP::GenerateReport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IGPMRSOP.GenerateReport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMRSOP::GenerateReport


## -description


The <a href="https://msdn.microsoft.com/d5daa512-547f-4b2d-85b3-0f6e9244acb2">GenerateReport</a> method generates a report on the RSoP data.


## -parameters




### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.


### -param pvarGPMProgress [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of report generation. If this parameter is not <b>NULL</b>, the call to <b>GenerateReport</b> is handled asynchronously. If this parameter is <b>NULL</b> the call to <b>GenerateReport</b> is handled synchronously and a pointer to a <a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface is returned in <i>pvarGPMCancel</i>. This parameter must be <b>NULL</b> if the client should not receive asynchronous notifications.


### -param pvarGPMCancel [out, optional]

Receives a pointer to an <a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface that the client can use to cancel the report generation. This parameter is not returned when <i>pvarGPMProgress</i> is <b>NULL</b>.


### -param ppIGPMResult [out]

Pointer to an <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a>. The <b>Result</b> property contains  a binary string of XML or HTML. The <a href="https://msdn.microsoft.com/8570d40c-25c2-405c-b52a-dae6c0eb50e0">Status</a> property contains a reference to an <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.




## -see-also




<a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">IGPMRSOP</a>
 

 

