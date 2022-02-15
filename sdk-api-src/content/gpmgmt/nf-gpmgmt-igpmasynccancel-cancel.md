---
UID: NF:gpmgmt.IGPMAsyncCancel.Cancel
title: IGPMAsyncCancel::Cancel (gpmgmt.h)
description: The client calls this method to cancel an asynchronous Group Policy Management Console (GPMC) operation. GPMC operations such as backup, restore, import, copy, and report generation can execute asynchronously.
helpviewer_keywords: ["Cancel","Cancel method [GPMC]","Cancel method [GPMC]","IGPMAsyncCancel interface","IGPMAsyncCancel interface [GPMC]","Cancel method","IGPMAsyncCancel.Cancel","IGPMAsyncCancel::Cancel","_win32_igpmasynccancel_cancel","gpmc.igpmasynccancel_cancel","gpmgmt/IGPMAsyncCancel::Cancel"]
old-location: gpmc\igpmasynccancel_cancel.htm
tech.root: gpmc
ms.assetid: c2055e7d-daed-4c9c-a374-6cb378d04962
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [GPMC], Cancel method [GPMC],IGPMAsyncCancel interface, IGPMAsyncCancel interface [GPMC],Cancel method, IGPMAsyncCancel.Cancel, IGPMAsyncCancel::Cancel, _win32_igpmasynccancel_cancel, gpmc.igpmasynccancel_cancel, gpmgmt/IGPMAsyncCancel::Cancel
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMAsyncCancel::Cancel
 - gpmgmt/IGPMAsyncCancel::Cancel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMAsyncCancel.Cancel
---

# IGPMAsyncCancel::Cancel


## -description

The client calls this method to cancel an asynchronous Group Policy Management Console (GPMC) operation. GPMC operations such as backup, restore, import, copy, and report generation can execute asynchronously.



## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a>
