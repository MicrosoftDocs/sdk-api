---
UID: NF:gpmgmt.IGPMStarterGPO.GenerateReportToFile
title: IGPMStarterGPO::GenerateReportToFile
author: windows-sdk-content
description: The GenerateReportToFile method gets the report for the GPO and saves it to a file at a specified path.
old-location: gpmc\igpmstartergpo_generatereporttofile.htm
old-project: GPMC
ms.assetid: 29302091-0f2d-4511-a25b-9af078795d1d
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GenerateReportToFile, GenerateReportToFile method [GPMC], GenerateReportToFile method [GPMC],IGPMStarterGPO interface, IGPMStarterGPO interface [GPMC],GenerateReportToFile method, IGPMStarterGPO.GenerateReportToFile, IGPMStarterGPO::GenerateReportToFile, gpmc.igpmstartergpo_generatereporttofile, gpmgmt/IGPMStarterGPO::GenerateReportToFile
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
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	gpmgmt.dll
api_name:
-	IGPMStarterGPO.GenerateReportToFile
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMStarterGPO::GenerateReportToFile


## -description


The <b>GenerateReportToFile</b> method gets the report for the GPO and saves it to a file at a specified path.


## -parameters




### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.


### -param bstrTargetFilePath [in]

Binary string that contains the path to the file where the report is being saved. Use null-terminated string.


### -param ppIGPMResult [out]

Pointer to an <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface. The <b>Status</b> property contains a reference to an <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property of the <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface is indeterminate and should not be relied upon.</div>
<div> </div>

## -returns



Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">IGPMStarterGPO</a>
 

 

