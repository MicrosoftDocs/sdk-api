---
UID: NF:msvidctl.IMSVidCtl.Decompose
title: IMSVidCtl::Decompose
author: windows-sdk-content
description: The Decompose method tears down the filter graph.
old-location: mstv\imsvidctl_decompose.htm
tech.root: mstv
ms.assetid: e67bf380-dc2c-42c9-a995-17951c65fbda
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Decompose, Decompose method [Microsoft TV Technologies], Decompose method [Microsoft TV Technologies],IMSVidCtl interface, IMSVidCtl interface [Microsoft TV Technologies],Decompose method, IMSVidCtl.Decompose, IMSVidCtl::Decompose, IMSVidCtlDecompose, mstv.imsvidctl_decompose, msvidctl/IMSVidCtl::Decompose
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
 - IMSVidCtl.Decompose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidCtl::Decompose


## -description


The <b>Decompose</b> method tears down the filter graph.


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is the inverse of the <a href="https://msdn.microsoft.com/49f78dd8-f26e-456d-b67e-155ae0ed5419">IMSVidCtl::Build</a> method. Call this method before you change the Active Features collection, specify a new renderer, or specify a new input device. The method does not modify the Active Features collection.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>
 

 

