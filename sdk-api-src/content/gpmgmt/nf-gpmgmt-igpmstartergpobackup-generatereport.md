---
UID: NF:gpmgmt.IGPMStarterGPOBackup.GenerateReport
title: IGPMStarterGPOBackup::GenerateReport (gpmgmt.h)
author: windows-sdk-content
description: The GenerateReport method gets the report for the backup GPO.
old-location: gpmc\igpmstartergpobackup_generatereport.htm
tech.root: gpmc
ms.assetid: ce0dd44f-dfd9-4e7c-9854-9decbc25ec54
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GenerateReport, GenerateReport method [GPMC], GenerateReport method [GPMC],IGPMStarterGPOBackup interface, IGPMStarterGPOBackup interface [GPMC],GenerateReport method, IGPMStarterGPOBackup.GenerateReport, IGPMStarterGPOBackup::GenerateReport, gpmc.igpmstartergpobackup_generatereport, gpmgmt/IGPMStarterGPOBackup::GenerateReport
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
 - IGPMStarterGPOBackup.GenerateReport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMStarterGPOBackup::GenerateReport


## -description


The <a href="https://msdn.microsoft.com/d5daa512-547f-4b2d-85b3-0f6e9244acb2">GenerateReport</a> method gets the report for the backup GPO.


## -parameters




### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.


### -param pvarGPMProgress [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a> interface. If <i>pvarGPMProgress</i> is null, the call to <a href="https://msdn.microsoft.com/d5daa512-547f-4b2d-85b3-0f6e9244acb2">GenerateReport</a> is handled synchronously. If  not null, the call to <b>GenerateReport</b> is handled asynchronously and <i>pvarGPMCancel</i> returns a pointer to   <a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a>.


### -param pvarGPMCancel [out, optional]

Pointer to an <a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface. A value for this parameter is returned only when <i>pvarGPMProgress</i> is specified and is not null.


### -param ppIGPMResult [out]

Pointer to an <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a>. The Result property contains  a string of XML or HTML. The Status property contains a reference to an  <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.




## -see-also




<a href="https://msdn.microsoft.com/3008e70c-cc34-45b0-bdfc-17f2e9cd5de0">IGPMBackupDirEx</a>



<a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">IGPMStarterGPOBackup</a>



<a href="https://msdn.microsoft.com/df9f29d0-8636-4393-8f7e-c9e22f3692f5">IGPMStarterGPOBackupCollection</a>
 

 

