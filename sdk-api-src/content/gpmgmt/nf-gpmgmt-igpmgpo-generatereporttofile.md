---
UID: NF:gpmgmt.IGPMGPO.GenerateReportToFile
title: IGPMGPO::GenerateReportToFile method
author: windows-driver-content
description: Gets the report for a GPO and then saves the report to a file in a specified path.
old-location: gpmc\igpmgpo_generatereporttofile.htm
old-project: GPMC
ms.assetid: 686b1461-3136-4351-adc4-32d558d62246
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GenerateReportToFile method [GPMC], GenerateReportToFile method [GPMC], IGPMGPO interface, GenerateReportToFile,IGPMGPO.GenerateReportToFile, IGPMGPO, IGPMGPO interface [GPMC], GenerateReportToFile method, IGPMGPO::GenerateReportToFile, gpmc.igpmgpo_generatereporttofile, gpmgmt/IGPMGPO::GenerateReportToFile
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
-	IGPMGPO.GenerateReportToFile
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMGPO::GenerateReportToFile method


## -description


Gets the report for a GPO and then saves the report to a file in a specified path.


## -parameters




### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.


### -param bstrTargetFilePath [in]

Binary string that contains the path of the file in which the report is being saved. Use a null-terminated string.


### -param ppIGPMResult [out]

Pointer to an <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface. The <b>Status</b> property contains a reference to an <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property of the <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface is indeterminate and should not be relied upon.</div>
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




<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>
 

 

