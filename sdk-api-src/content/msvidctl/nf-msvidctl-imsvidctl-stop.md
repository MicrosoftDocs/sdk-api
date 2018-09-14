---
UID: NF:msvidctl.IMSVidCtl.Stop
title: IMSVidCtl::Stop
author: windows-sdk-content
description: The Stop method stops the filter graph.
old-location: mstv\imsvidctl_stop.htm
tech.root: MSTV
ms.assetid: 8ca43663-3726-4147-8774-2f1eecef9142
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],Stop method, IMSVidCtl.Stop, IMSVidCtl::Stop, IMSVidCtlStop, Stop, Stop method [Microsoft TV Technologies], Stop method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_stop, msvidctl/IMSVidCtl::Stop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.Stop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidCtl::Stop


## -description


The <b>Stop</b> method stops the filter graph.


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method leaves the filter graph intact and ready to pause or run. To tear down the filter graph, use the <a href="https://msdn.microsoft.com/e67bf380-dc2c-42c9-a995-17951c65fbda">IMSVidCtl::Decompose</a> method.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>
 

 

