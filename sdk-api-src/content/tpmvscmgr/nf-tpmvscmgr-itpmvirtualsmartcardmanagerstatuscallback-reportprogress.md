---
UID: NF:tpmvscmgr.ITpmVirtualSmartCardManagerStatusCallback.ReportProgress
title: ITpmVirtualSmartCardManagerStatusCallback::ReportProgress (tpmvscmgr.h)
author: windows-sdk-content
description: Reports the progress of the current operation.
old-location: security\itpmvirtualsmartcardmanagerstatuscallback_reportprogress.htm
tech.root: SecAuthN
ms.assetid: E20CF68F-0DFB-48E4-9B68-83A8E8763424
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITpmVirtualSmartCardManagerStatusCallback interface [Security],ReportProgress method, ITpmVirtualSmartCardManagerStatusCallback.ReportProgress, ITpmVirtualSmartCardManagerStatusCallback::ReportProgress, ReportProgress, ReportProgress method [Security], ReportProgress method [Security],ITpmVirtualSmartCardManagerStatusCallback interface, security.itpmvirtualsmartcardmanagerstatuscallback_reportprogress, tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback::ReportProgress
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITpmVirtualSmartCardManagerStatusCallback::ReportProgress


## -description


Reports the progress of the current operation.


## -parameters




### -param Status [in]

Status code of the current operation from the possible status states listed in the <a href="https://docs.microsoft.com/windows/desktop/api/tpmvscmgr/ne-tpmvscmgr-__midl___midl_itf_tpmvscmgr_0000_0000_0001">TPMVSCMGR_STATUS</a> enumeration.


## -returns



If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns a Win32 error code. The requested operation on the TPM virtual smart card manager server may be interrupted.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tpmvscmgr/nn-tpmvscmgr-itpmvirtualsmartcardmanagerstatuscallback">ITpmVirtualSmartCardManagerStatusCallback</a>
 

 

