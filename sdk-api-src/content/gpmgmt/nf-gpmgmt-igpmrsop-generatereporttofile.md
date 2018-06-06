---
UID: NF:gpmgmt.IGPMRSOP.GenerateReportToFile
title: IGPMRSOP::GenerateReportToFile
author: windows-sdk-content
description: The GenerateReportToFile method generates a report on the RSoP data and saves it to a file at a specified path.
old-location: gpmc\igpmrsop_generatereporttofile.htm
old-project: GPMC
ms.assetid: 92a199d6-244f-44e5-8158-d77b8488fde0
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GenerateReportToFile, GenerateReportToFile method [GPMC], GenerateReportToFile method [GPMC],IGPMRSOP interface, IGPMRSOP interface [GPMC],GenerateReportToFile method, IGPMRSOP.GenerateReportToFile, IGPMRSOP::GenerateReportToFile, gpmc.igpmrsop_generatereporttofile, gpmgmt/IGPMRSOP::GenerateReportToFile
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMRSOP.GenerateReportToFile
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMRSOP::GenerateReportToFile


## -description


The <b>GenerateReportToFile</b> method generates a report on the RSoP data and saves it to a file at a specified path.


## -parameters




### -param gpmReportType [in]

Specifies whether the report is in XML or HTML.


### -param bstrTargetFilePath [in]

Binary string that contains the path to the file where the report is being saved. Use null-terminated string.

<div class="alert"><b>Note</b>  If the path to the file is not specified, then the report will be created in the "%windir%\system32\" directory.</div>
<div> </div>

### -param ppIGPMResult [out]

Pointer to an <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface. The <b>Status</b> property contains a reference to an <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>.

<div class="alert"><b>Note</b>  The value of the <b>Result</b> property of the <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface is indeterminate and should not be relied upon.</div>
<div> </div>

#### - TargetFile [in]

Binary string that contains the path to the file where the report is being saved.

<div class="alert"><b>Note</b>  If the path to the file is not specified, then the report will be created in the "%windir%\system32\" directory.</div>
<div> </div>

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




<a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">IGPMRSOP</a>
 

 

