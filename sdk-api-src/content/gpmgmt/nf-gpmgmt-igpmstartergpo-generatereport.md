---
UID: NF:gpmgmt.IGPMStarterGPO.GenerateReport
title: IGPMStarterGPO::GenerateReport
author: windows-sdk-content
description: Gets the report for the Starter GPO.
old-location: gpmc\igpmstartergpo_generatereport.htm
tech.root: GPMC
ms.assetid: 127cde40-abe0-42da-9845-2fe1c0b1f1f1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GenerateReport, GenerateReport method [GPMC], GenerateReport method [GPMC],IGPMStarterGPO interface, IGPMStarterGPO interface [GPMC],GenerateReport method, IGPMStarterGPO.GenerateReport, IGPMStarterGPO::GenerateReport, gpmc.igpmstartergpo_generatereport, gpmgmt/IGPMStarterGPO::GenerateReport
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
 - gpmgmt.dll
api_name:
 - IGPMStarterGPO.GenerateReport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMStarterGPO::GenerateReport


## -description


 Gets the report for the Starter GPO.


## -parameters




### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.


### -param pvarGPMProgress [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the copy operation. If not <b>NULL</b>, the call to <a href="https://msdn.microsoft.com/d5daa512-547f-4b2d-85b3-0f6e9244acb2">GenerateReport</a> is handled asynchronously and <i>pvarGPMCancel</i> receives a pointer to an <a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface.   If this parameter is <b>NULL</b> the call to <b>GenerateReport</b> is handled synchronously. The <i>pvarGPMProgress</i> parameter must be <b>NULL</b> if the client should not receive asynchronous notifications.


### -param pvarGPMCancel [in, optional]

Receives a pointer to an <a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface that the client can use to cancel the copy operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.


### -param ppIGPMResult [out]

Pointer to an <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a>. The Result property contains  a binary string of XML or HTML. The Status property contains a reference to an <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>.


## -returns



Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">IGPMStarterGPO</a>
 

 

