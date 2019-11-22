---
UID: NF:msvidctl.IMSVidCtl.Run
title: IMSVidCtl::Run (msvidctl.h)

description: The Run method runs the filter graph.
old-location: mstv\imsvidctl_run.htm
tech.root: mstv
ms.assetid: 37ed6d7b-2e44-4bce-b476-8e8b28635346

ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],Run method, IMSVidCtl.Run, IMSVidCtl::Run, IMSVidCtlRun, Run, Run method [Microsoft TV Technologies], Run method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_run, msvidctl/IMSVidCtl::Run
ms.topic: method
f1_keywords: 
 - "msvidctl/IMSVidCtl.Run"
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
 - IMSVidCtl.Run
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidCtl::Run


## -description


The <b>Run</b> method runs the filter graph.


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method builds the filter graph if the state is unbuilt, and puts the graph into the running state. For more information on the behavior of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-build">Build</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">View</a> and <b>Run</b>, see <b>IMSVidCtl::View</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>
 

 

