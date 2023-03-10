---
UID: NN:gpmgmt.IGPMAsyncCancel
title: IGPMAsyncCancel (gpmgmt.h)
description: A pointer to the IGPMAsyncCancel interface is returned to the client by the Group Policy Management Console (GPMC) method that the client calls asynchronously.
helpviewer_keywords: ["GPMAsyncCancel","IGPMAsyncCancel","IGPMAsyncCancel interface [GPMC]","IGPMAsyncCancel interface [GPMC]","described","_win32_igpmasynccancel","gpmc.igpmasynccancel","gpmgmt/IGPMAsyncCancel"]
old-location: gpmc\igpmasynccancel.htm
tech.root: gpmc
ms.assetid: 74b2bb04-6118-4fd1-83c0-3549db3f35f3
ms.date: 12/05/2018
ms.keywords: GPMAsyncCancel, IGPMAsyncCancel, IGPMAsyncCancel interface [GPMC], IGPMAsyncCancel interface [GPMC],described, _win32_igpmasynccancel, gpmc.igpmasynccancel, gpmgmt/IGPMAsyncCancel
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
 - IGPMAsyncCancel
 - gpmgmt/IGPMAsyncCancel
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
 - IGPMAsyncCancel
 - GPMAsyncCancel
---

# IGPMAsyncCancel interface


## -description

A pointer to the 
<b>IGPMAsyncCancel</b> interface is returned to the client by the Group Policy Management Console (GPMC) method that the client calls asynchronously. GPMC operations such as backup, restore, import, copy, and report generation can execute asynchronously. This object cannot be accessed through scripting.

## -inheritance

The <b>IGPMAsyncCancel</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMAsyncCancel</b> also has these types of members:

## -remarks

GPMC operations such as backup, restore, import, copy, and report generation can execute asynchronously. For more information about how to use this interface with asynchronous operations, see the "Remarks" section of 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress Interface</a>. The server calls 
the <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmasyncprogress-status">IGPMAsyncProgress::Status</a> method to notify the client about the progress of the operation. The 
<b>Status</b> method also returns an interface pointer to the resultant object, for example, to a <b>GPMGPO</b> or to a <b>GPMBackup</b> object. The caller can then cancel the operation by calling the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmasynccancel-cancel">IGPMAsyncCancel::Cancel</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a>
