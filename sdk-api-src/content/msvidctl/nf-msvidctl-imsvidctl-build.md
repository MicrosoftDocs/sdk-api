---
UID: NF:msvidctl.IMSVidCtl.Build
title: IMSVidCtl::Build (msvidctl.h)
author: windows-sdk-content
description: The Build method builds the filter graph and connects all the filters.
old-location: mstv\imsvidctl_build.htm
tech.root: mstv
ms.assetid: 49f78dd8-f26e-456d-b67e-155ae0ed5419
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Build, Build method [Microsoft TV Technologies], Build method [Microsoft TV Technologies],IMSVidCtl interface, IMSVidCtl interface [Microsoft TV Technologies],Build method, IMSVidCtl.Build, IMSVidCtl::Build, IMSVidCtlBuild, mstv.imsvidctl_build, msvidctl/IMSVidCtl::Build
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
 - IMSVidCtl.Build
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidCtl::Build


## -description


The <b>Build</b> method builds the filter graph and connects all the filters.


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method builds a filter graph using the current input device. To select an input device, call the <a href="https://msdn.microsoft.com/ec0e2a88-13c0-42f3-ba7d-8ebff1234b86">IMSVidCtl::View</a> method or the <a href="https://msdn.microsoft.com/696d8ece-a377-4fe8-a790-a68d1a24e65a">IMSVidCtl::put_InputActive</a> method. If no input device has been selected, the method fails.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/e67bf380-dc2c-42c9-a995-17951c65fbda">IMSVidCtl::Decompose</a>
 

 

