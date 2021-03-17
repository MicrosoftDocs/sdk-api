---
UID: NF:tpmvscmgr.ITpmVirtualSmartCardManagerStatusCallback.ReportProgress
title: ITpmVirtualSmartCardManagerStatusCallback::ReportProgress (tpmvscmgr.h)
description: Reports the progress of the current operation.
helpviewer_keywords: ["ITpmVirtualSmartCardManagerStatusCallback interface [Security]","ReportProgress method","ITpmVirtualSmartCardManagerStatusCallback.ReportProgress","ITpmVirtualSmartCardManagerStatusCallback::ReportProgress","ReportProgress","ReportProgress method [Security]","ReportProgress method [Security]","ITpmVirtualSmartCardManagerStatusCallback interface","security.itpmvirtualsmartcardmanagerstatuscallback_reportprogress","tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback::ReportProgress"]
old-location: security\itpmvirtualsmartcardmanagerstatuscallback_reportprogress.htm
tech.root: security
ms.assetid: E20CF68F-0DFB-48E4-9B68-83A8E8763424
ms.date: 12/05/2018
ms.keywords: ITpmVirtualSmartCardManagerStatusCallback interface [Security],ReportProgress method, ITpmVirtualSmartCardManagerStatusCallback.ReportProgress, ITpmVirtualSmartCardManagerStatusCallback::ReportProgress, ReportProgress, ReportProgress method [Security], ReportProgress method [Security],ITpmVirtualSmartCardManagerStatusCallback interface, security.itpmvirtualsmartcardmanagerstatuscallback_reportprogress, tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback::ReportProgress
req.header: tpmvscmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tpmvscmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vscmgr.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITpmVirtualSmartCardManagerStatusCallback::ReportProgress
 - tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback::ReportProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vscmgr.lib
 - Vscmgr.dll
api_name:
 - ITpmVirtualSmartCardManagerStatusCallback.ReportProgress
---

# ITpmVirtualSmartCardManagerStatusCallback::ReportProgress


## -description

Reports the progress of the current operation.

## -parameters

### -param Status [in]

Status code of the current operation from the possible status states listed in the <a href="/windows/win32/api/tpmvscmgr/ne-tpmvscmgr-tpmvscmgr_status">TPMVSCMGR_STATUS</a> enumeration.

## -returns

If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns a Win32 error code. The requested operation on the TPM virtual smart card manager server may be interrupted.

## -see-also

<a href="/windows/desktop/api/tpmvscmgr/nn-tpmvscmgr-itpmvirtualsmartcardmanagerstatuscallback">ITpmVirtualSmartCardManagerStatusCallback</a>