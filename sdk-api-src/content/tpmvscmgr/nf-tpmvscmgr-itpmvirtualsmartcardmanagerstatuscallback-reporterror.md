---
UID: NF:tpmvscmgr.ITpmVirtualSmartCardManagerStatusCallback.ReportError
title: ITpmVirtualSmartCardManagerStatusCallback::ReportError
author: windows-sdk-content
description: Reports any errors from the requested operation.
old-location: security\itpmvirtualsmartcardmanagerstatuscallback_reporterror.htm
tech.root: secauthn
ms.assetid: 936F22EA-1C9F-4328-B71F-FA7720396F6F
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ITpmVirtualSmartCardManagerStatusCallback interface [Security],ReportError method, ITpmVirtualSmartCardManagerStatusCallback.ReportError, ITpmVirtualSmartCardManagerStatusCallback::ReportError, ReportError, ReportError method [Security], ReportError method [Security],ITpmVirtualSmartCardManagerStatusCallback interface, security.itpmvirtualsmartcardmanagerstatuscallback_reporterror, tpmvscmgr/ITpmVirtualSmartCardManagerStatusCallback::ReportError
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
 - ITpmVirtualSmartCardManagerStatusCallback.ReportError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITpmVirtualSmartCardManagerStatusCallback::ReportError


## -description


Reports any errors from the requested operation.


## -parameters




### -param Error [in]

Error code of the current error from the possible errors listed in the <a href="https://msdn.microsoft.com/0B8A5703-DA7C-4FD6-A39E-BA2CE172ADF9">TPMVSCMGR_ERROR</a> enumeration.


## -returns



If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns a Win32 error code. The requested operation on the TPM virtual smart card manager server may be interrupted.




## -see-also




<a href="https://msdn.microsoft.com/6CB62E42-16FD-453F-9566-B4DFCDAC7368">ITpmVirtualSmartCardManagerStatusCallback</a>
 

 

