---
UID: NF:tpmvscmgr.ITpmVirtualSmartCardManagerStatusCallback.ReportError
title: ITpmVirtualSmartCardManagerStatusCallback::ReportError (tpmvscmgr.h)
description: Reports any errors from the requested operation.
helpviewer_keywords: ["ITpmVirtualSmartCardManagerStatusCallback interface [Security]","ReportError method","ITpmVirtualSmartCardManagerStatusCallback.ReportError","ITpmVirtualSmartCardManagerStatusCallback::ReportError","ReportError","ReportError method [Security]","ReportError method [Security]","ITpmVirtualSmartCardManagerStatusCallback interface","security.itpmvirtualsmartcardmanagerstatuscallback_reporterror","tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback::ReportError"]
old-location: security\itpmvirtualsmartcardmanagerstatuscallback_reporterror.htm
tech.root: security
ms.assetid: 936F22EA-1C9F-4328-B71F-FA7720396F6F
ms.date: 12/05/2018
ms.keywords: ITpmVirtualSmartCardManagerStatusCallback interface [Security],ReportError method, ITpmVirtualSmartCardManagerStatusCallback.ReportError, ITpmVirtualSmartCardManagerStatusCallback::ReportError, ReportError, ReportError method [Security], ReportError method [Security],ITpmVirtualSmartCardManagerStatusCallback interface, security.itpmvirtualsmartcardmanagerstatuscallback_reporterror, tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback::ReportError
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
 - ITpmVirtualSmartCardManagerStatusCallback::ReportError
 - tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback::ReportError
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
 - ITpmVirtualSmartCardManagerStatusCallback.ReportError
---

# ITpmVirtualSmartCardManagerStatusCallback::ReportError


## -description

Reports any errors from the requested operation.

## -parameters

### -param Error [in]

Error code of the current error from the possible errors listed in the <a href="/windows/win32/api/tpmvscmgr/ne-tpmvscmgr-tpmvscmgr_error">TPMVSCMGR_ERROR</a> enumeration.

## -returns

If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns a Win32 error code. The requested operation on the TPM virtual smart card manager server may be interrupted.

## -see-also

<a href="/windows/desktop/api/tpmvscmgr/nn-tpmvscmgr-itpmvirtualsmartcardmanagerstatuscallback">ITpmVirtualSmartCardManagerStatusCallback</a>