---
UID: NF:msvidctl.IMSVidCtl.Run
title: IMSVidCtl::Run (msvidctl.h)
description: The Run method runs the filter graph.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","Run method","IMSVidCtl.Run","IMSVidCtl::Run","IMSVidCtlRun","Run","Run method [Microsoft TV Technologies]","Run method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_run","msvidctl/IMSVidCtl::Run"]
old-location: mstv\imsvidctl_run.htm
tech.root: mstv
ms.assetid: 37ed6d7b-2e44-4bce-b476-8e8b28635346
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],Run method, IMSVidCtl.Run, IMSVidCtl::Run, IMSVidCtlRun, Run, Run method [Microsoft TV Technologies], Run method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_run, msvidctl/IMSVidCtl::Run
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidCtl::Run
 - msvidctl/IMSVidCtl::Run
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.Run
---

# IMSVidCtl::Run


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Run</b> method runs the filter graph.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method builds the filter graph if the state is unbuilt, and puts the graph into the running state. For more information on the behavior of <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-build">Build</a>, <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">View</a> and <b>Run</b>, see <b>IMSVidCtl::View</b>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>
