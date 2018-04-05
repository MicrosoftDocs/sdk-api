---
UID: NF:msvidctl.IMSVidCtl.Refresh
title: IMSVidCtl::Refresh method
author: windows-driver-content
description: The Refresh method immediately updates the Video Control's appearance.
old-location: mstv\imsvidctl_refresh.htm
old-project: mstv
ms.assetid: 7413049e-3ce4-46e9-ab49-fbdb0455c6b6
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidCtl, IMSVidCtl interface [Microsoft TV Technologies], Refresh method, IMSVidCtl::Refresh, IMSVidCtlRefresh, Refresh method [Microsoft TV Technologies], Refresh method [Microsoft TV Technologies], IMSVidCtl interface, Refresh,IMSVidCtl.Refresh, mstv.imsvidctl_refresh, msvidctl/IMSVidCtl::Refresh
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
-	IMSVidCtl.Refresh
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidCtl::Refresh method


## -description


The <b>Refresh</b> method immediately updates the Video Control's appearance.


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is a stock ActiveX control method. It forces the Video Control window to repaint itself. Before repainting, the Video Control ensures that the video rectangle is up to date and that all Video Mixing Renderer settings are correct.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>
 

 

