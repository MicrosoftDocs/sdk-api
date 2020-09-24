---
UID: NF:gpmgmt.IGPMStarterGPO.CopyTo
title: IGPMStarterGPO::CopyTo (gpmgmt.h)
description: The CopyTo method copies the current Starter GPO and returns a pointer to the copy of the Starter GPO.
helpviewer_keywords: ["CopyTo","CopyTo method [GPMC]","CopyTo method [GPMC]","IGPMStarterGPO interface","IGPMStarterGPO interface [GPMC]","CopyTo method","IGPMStarterGPO.CopyTo","IGPMStarterGPO::CopyTo","gpmc.igpmstartergpo_copyto","gpmgmt/IGPMStarterGPO::CopyTo"]
old-location: gpmc\igpmstartergpo_copyto.htm
tech.root: gpmc
ms.assetid: 28639323-5253-4f63-b1b1-4fd75abaa2b4
ms.date: 12/05/2018
ms.keywords: CopyTo, CopyTo method [GPMC], CopyTo method [GPMC],IGPMStarterGPO interface, IGPMStarterGPO interface [GPMC],CopyTo method, IGPMStarterGPO.CopyTo, IGPMStarterGPO::CopyTo, gpmc.igpmstartergpo_copyto, gpmgmt/IGPMStarterGPO::CopyTo
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
 - IGPMStarterGPO::CopyTo
 - gpmgmt/IGPMStarterGPO::CopyTo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gpmgmt.dll
api_name:
 - IGPMStarterGPO.CopyTo
---

# IGPMStarterGPO::CopyTo


## -description

The <b>CopyTo</b> method copies the current Starter GPO and returns a pointer to the copy of the Starter GPO.  The method copies all the contents of the Starter GPO but creates the new Starter GPO with the default new Starter GPO delegation settings.  Copying a system Starter GPO creates a new custom Starter GPO.

## -parameters

### -param pvarNewDisplayName [in, optional]

Display name to be put on the copied Starter GPO. A display name is assigned if the <b>VARIANT</b> structure does not contain a <b>BSTR</b>, or if <i>pvarNewDisplayName</i> is <b>NULL</b>.

### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the copy operation. This parameter must be <b>NULL</b> if the client does not receive asynchronous notifications.

### -param pvarGPMCancel [in, optional]

Receives a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface that the client can use to cancel the copy operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.

### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface that represents the result of the copy operation. That interface contains pointers to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a> interface and an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a> interface.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

For more information, see the following Remarks section.

## -remarks

Note that you must check the code returned by the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmresult-overallstatus">IGPMResult::OverallStatus</a> method as well as the one returned by this method to determine whether or not the operation succeeded. 
<b>OverallStatus</b> returns an overall status code for the operation. If no error occurred during the operation, it returns a success code; otherwise it returns a failure code.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">IGPMStarterGPO</a>