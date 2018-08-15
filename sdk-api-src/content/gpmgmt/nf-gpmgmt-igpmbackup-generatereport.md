---
UID: NF:gpmgmt.IGPMBackup.GenerateReport
title: IGPMBackup::GenerateReport
author: windows-sdk-content
description: Gets the report for the backup Group Policy object (GPO).
old-location: gpmc\igpmbackup_generatereport.htm
old-project: GPMC
ms.assetid: d5daa512-547f-4b2d-85b3-0f6e9244acb2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMBackup object [GPMC],GenerateReport method, GenerateReport, GenerateReport method [GPMC], GenerateReport method [GPMC],GPMBackup object, GenerateReport method [GPMC],IGPMBackup interface, IGPMBackup interface [GPMC],GenerateReport method, IGPMBackup.GenerateReport, IGPMBackup::GenerateReport, gpmc.igpmbackup_generatereport, gpmgmt/IGPMBackup::GenerateReport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMBackup.GenerateReport
 - GPMBackup.GenerateReport
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMBackup::GenerateReport


## -description


Gets the report for the backup Group Policy object (GPO).


## -parameters




### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.


### -param pvarGPMProgress [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a> interface. If <i>pvarGPMProgress</i> is <b>NULL</b>, the call to <b>GenerateReport</b> is handled synchronously. If  not <b>NULL</b>, the call to <b>GenerateReport</b> is handled asynchronously, and<i>pvarGPMCancel</i> returns a pointer to    <a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> .


### -param pvarGPMCancel [out, optional]

Pointer to an <a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface. A value for this parameter is returned only when <i>pvarGPMProgress</i> is specified and is not <b>NULL</b>.


### -param ppIGPMResult [out]

Pointer to an <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface. The <b>Result</b> property contains  a string of XML or HTML. The <b>Status</b> property contains a reference to an  <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.




## -see-also




<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMBackupCollection</a>



<a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">IGPMBackupDir</a>
 

 

