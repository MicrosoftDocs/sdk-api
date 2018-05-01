---
UID: NF:tpmvscmgr.ITpmVirtualSmartCardManagerStatusCallback.ReportProgress
title: ITpmVirtualSmartCardManagerStatusCallback::ReportProgress method
author: windows-driver-content
description: Reports the progress of the current operation.
old-location: security\itpmvirtualsmartcardmanagerstatuscallback_reportprogress.htm
old-project: SecAuthN
ms.assetid: E20CF68F-0DFB-48E4-9B68-83A8E8763424
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ITpmVirtualSmartCardManagerStatusCallback, ITpmVirtualSmartCardManagerStatusCallback interface [Security], ReportProgress method, ITpmVirtualSmartCardManagerStatusCallback::ReportProgress, ReportProgress method [Security], ReportProgress method [Security], ITpmVirtualSmartCardManagerStatusCallback interface, ReportProgress,ITpmVirtualSmartCardManagerStatusCallback.ReportProgress, security.itpmvirtualsmartcardmanagerstatuscallback_reportprogress, tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback::ReportProgress
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TPMVSCMGR_ERROR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vscmgr.lib
-	Vscmgr.dll
api_name:
-	ITpmVirtualSmartCardManagerStatusCallback.ReportProgress
product: Windows
targetos: Windows
req.lib: Vscmgr.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITpmVirtualSmartCardManagerStatusCallback::ReportProgress method


## -description


Reports the progress of the current operation.


## -parameters




### -param Status [in]

Status code of the current operation from the possible status states listed in the <a href="https://msdn.microsoft.com/9E678584-D225-4BDD-8035-92818B977DE9">TPMVSCMGR_STATUS</a> enumeration.


## -returns



If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns a Win32 error code. The requested operation on the TPM virtual smart card manager server may be interrupted.




## -see-also




<a href="https://msdn.microsoft.com/6CB62E42-16FD-453F-9566-B4DFCDAC7368">ITpmVirtualSmartCardManagerStatusCallback</a>
 

 

