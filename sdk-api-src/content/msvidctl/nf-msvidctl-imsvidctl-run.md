---
UID: NF:msvidctl.IMSVidCtl.Run
title: IMSVidCtl::Run method
author: windows-driver-content
description: The Run method runs the filter graph.
old-location: mstv\imsvidctl_run.htm
old-project: mstv
ms.assetid: 37ed6d7b-2e44-4bce-b476-8e8b28635346
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidCtl, IMSVidCtl interface [Microsoft TV Technologies], Run method, IMSVidCtl::Run, IMSVidCtlRun, Run method [Microsoft TV Technologies], Run method [Microsoft TV Technologies], IMSVidCtl interface, Run,IMSVidCtl.Run, mstv.imsvidctl_run, msvidctl/IMSVidCtl::Run
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msvidctl.h
api_name:
-	IMSVidCtl.Run
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidCtl::Run method


## -description


The <b>Run</b> method runs the filter graph.


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method builds the filter graph if the state is unbuilt, and puts the graph into the running state. For more information on the behavior of <a href="https://msdn.microsoft.com/49f78dd8-f26e-456d-b67e-155ae0ed5419">Build</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">View</a> and <b>Run</b>, see <b>IMSVidCtl::View</b>.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>
 

 

