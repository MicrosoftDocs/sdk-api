---
UID: NF:msvidctl.IMSVidCtl.Build
title: IMSVidCtl::Build (msvidctl.h)
description: The Build method builds the filter graph and connects all the filters.
helpviewer_keywords: ["Build","Build method [Microsoft TV Technologies]","Build method [Microsoft TV Technologies]","IMSVidCtl interface","IMSVidCtl interface [Microsoft TV Technologies]","Build method","IMSVidCtl.Build","IMSVidCtl::Build","IMSVidCtlBuild","mstv.imsvidctl_build","msvidctl/IMSVidCtl::Build"]
old-location: mstv\imsvidctl_build.htm
tech.root: mstv
ms.assetid: 49f78dd8-f26e-456d-b67e-155ae0ed5419
ms.date: 12/05/2018
ms.keywords: Build, Build method [Microsoft TV Technologies], Build method [Microsoft TV Technologies],IMSVidCtl interface, IMSVidCtl interface [Microsoft TV Technologies],Build method, IMSVidCtl.Build, IMSVidCtl::Build, IMSVidCtlBuild, mstv.imsvidctl_build, msvidctl/IMSVidCtl::Build
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
 - IMSVidCtl::Build
 - msvidctl/IMSVidCtl::Build
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
 - IMSVidCtl.Build
---

# IMSVidCtl::Build


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Build</b> method builds the filter graph and connects all the filters.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method builds a filter graph using the current input device. To select an input device, call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">IMSVidCtl::View</a> method or the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_inputactive">IMSVidCtl::put_InputActive</a> method. If no input device has been selected, the method fails.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-decompose">IMSVidCtl::Decompose</a>
