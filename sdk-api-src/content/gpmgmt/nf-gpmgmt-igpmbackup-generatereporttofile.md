---
UID: NF:gpmgmt.IGPMBackup.GenerateReportToFile
title: IGPMBackup::GenerateReportToFile
author: windows-sdk-content
description: The GenerateReportToFile method gets the report for the backup Group Policy object (GPO) and then saves the report to a file in a specified path.
old-location: gpmc\igpmbackup_generatereporttofile.htm
old-project: GPMC
ms.assetid: cba43c59-54d8-4d0b-b603-638f493cdf71
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GenerateReportToFile, GenerateReportToFile method [GPMC], GenerateReportToFile method [GPMC],IGPMBackup interface, IGPMBackup interface [GPMC],GenerateReportToFile method, IGPMBackup.GenerateReportToFile, IGPMBackup::GenerateReportToFile, gpmc.igpmbackup_generatereporttofile, gpmgmt/IGPMBackup::GenerateReportToFile
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMBackup.GenerateReportToFile
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMBackup::GenerateReportToFile


## -description


The <b>GenerateReportToFile</b> method gets the report for the backup Group Policy object (GPO) and then saves the report to a file in a specified path.


## -parameters




### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.


### -param bstrTargetFilePath [in]

Binary string that contains the path of the file in which the report is being saved. Use a null-terminated string.


### -param ppIGPMResult [out]

Pointer to an <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface. The <b>Status</b> property contains a reference to an <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a> interface.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property is indeterminate and should not be relied upon.</div>
<div> </div>

#### - TargetFile [in]

Binary string that contains the path of the file in which the report is being saved.


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




<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMBackupCollection</a>



<a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">IGPMBackupDir</a>
 

 

