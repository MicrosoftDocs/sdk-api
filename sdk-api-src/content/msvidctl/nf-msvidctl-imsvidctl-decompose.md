---
UID: NF:msvidctl.IMSVidCtl.Decompose
title: IMSVidCtl::Decompose (msvidctl.h)
author: windows-sdk-content
description: The Decompose method tears down the filter graph.
old-location: mstv\imsvidctl_decompose.htm
tech.root: mstv
ms.assetid: e67bf380-dc2c-42c9-a995-17951c65fbda
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Decompose, Decompose method [Microsoft TV Technologies], Decompose method [Microsoft TV Technologies],IMSVidCtl interface, IMSVidCtl interface [Microsoft TV Technologies],Decompose method, IMSVidCtl.Decompose, IMSVidCtl::Decompose, IMSVidCtlDecompose, mstv.imsvidctl_decompose, msvidctl/IMSVidCtl::Decompose
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
ms.custom: 19H1
---

# IMSVidCtl::Decompose


## -description


The <b>Decompose</b> method tears down the filter graph.


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is the inverse of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-build">IMSVidCtl::Build</a> method. Call this method before you change the Active Features collection, specify a new renderer, or specify a new input device. The method does not modify the Active Features collection.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>
 

 

