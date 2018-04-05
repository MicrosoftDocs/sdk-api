---
UID: NF:gpmgmt.IGPMStarterGPOBackup.GenerateReportToFile
title: IGPMStarterGPOBackup::GenerateReportToFile method
author: windows-driver-content
description: The GenerateReportToFile gets the report for the backup Starter GPO and saves it to a file at a specified path.
old-location: gpmc\igpmstartergpobackup_generatereporttofile.htm
old-project: GPMC
ms.assetid: d7d05436-acd7-4b80-93e4-ea80e3eb1fff
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GenerateReportToFile method [GPMC], GenerateReportToFile method [GPMC], IGPMStarterGPOBackup interface, GenerateReportToFile,IGPMStarterGPOBackup.GenerateReportToFile, IGPMStarterGPOBackup, IGPMStarterGPOBackup interface [GPMC], GenerateReportToFile method, IGPMStarterGPOBackup::GenerateReportToFile, gpmc.igpmstartergpobackup_generatereporttofile, gpmgmt/IGPMStarterGPOBackup::GenerateReportToFile
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
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMStarterGPOBackup.GenerateReportToFile
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMStarterGPOBackup::GenerateReportToFile method


## -description


The <a href="https://msdn.microsoft.com/cba43c59-54d8-4d0b-b603-638f493cdf71">GenerateReportToFile</a> gets the report for the backup Starter GPO and saves it to a file at a specified path.


## -parameters




### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.


### -param bstrTargetFilePath [in]

Binary string that contains the path to the file where the report is being saved. Use null-terminated string.


### -param ppIGPMResult [out]

Pointer to an <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface. The <b>Status</b> property contains a reference to an <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property is indeterminate and should not be relied upon.</div>
<div> </div>

#### - TargetFile [in]

Binary string that contains the path to the file where the report is being saved.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property is indeterminate and should not be relied upon.</div>
<div> </div>
<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property is indeterminate and should not be relied upon.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3008e70c-cc34-45b0-bdfc-17f2e9cd5de0">IGPMBackupDirEx</a>



<a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">IGPMStarterGPOBackup</a>



<a href="https://msdn.microsoft.com/df9f29d0-8636-4393-8f7e-c9e22f3692f5">IGPMStarterGPOBackupCollection</a>
 

 

