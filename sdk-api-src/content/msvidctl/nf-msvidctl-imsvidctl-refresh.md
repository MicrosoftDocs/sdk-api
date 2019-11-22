---
UID: NF:msvidctl.IMSVidCtl.Refresh
title: IMSVidCtl::Refresh (msvidctl.h)

description: The Refresh method immediately updates the Video Control's appearance.
old-location: mstv\imsvidctl_refresh.htm
tech.root: mstv
ms.assetid: 7413049e-3ce4-46e9-ab49-fbdb0455c6b6

ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],Refresh method, IMSVidCtl.Refresh, IMSVidCtl::Refresh, IMSVidCtlRefresh, Refresh, Refresh method [Microsoft TV Technologies], Refresh method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_refresh, msvidctl/IMSVidCtl::Refresh
ms.topic: method
f1_keywords: 
 - "msvidctl/IMSVidCtl.Refresh"
dev_langs:
 - c++
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
 - IMSVidCtl.Refresh
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidCtl::Refresh


## -description


The <b>Refresh</b> method immediately updates the Video Control's appearance.


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is a stock ActiveX control method. It forces the Video Control window to repaint itself. Before repainting, the Video Control ensures that the video rectangle is up to date and that all Video Mixing Renderer settings are correct.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>
 

 

