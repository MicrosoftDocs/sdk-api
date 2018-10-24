---
UID: NC:pdh.CounterPathCallBack
title: CounterPathCallBack
author: windows-sdk-content
description: Applications implement the CounterPathCallBack function to process the counter path strings returned by the Browse dialog box.
old-location: perf\counterpathcallback.htm
tech.root: perfctrs
ms.assetid: b7a2112e-9f50-4a36-b022-f9609b2827bc
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: CounterPathCallBack, CounterPathCallBack callback, CounterPathCallBack callback function [Perf], _win32_counterpathcallback, base.counterpathcallback, pdh/CounterPathCallBack, perf.counterpathcallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - UserDefined
api_location:
 - Pdh.h
api_name:
 - CounterPathCallBack
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CounterPathCallBack callback function


## -description


Applications implement the <b>CounterPathCallBack</b> function to process the counter path strings returned by the  <b>Browse</b> dialog box.
		


## -parameters




### -param Arg1








#### - dwArg [in]

User-defined value passed to the callback function by the <b>Browse</b> dialog box. You set this value in the <b>dwCallBackArg</b> member of the 
<a href="https://msdn.microsoft.com/8e045e0b-c157-4527-902c-6096c7922642">PDH_BROWSE_DLG_CONFIG</a> structure.


## -returns



Return ERROR_SUCCESS if the function succeeds. 

If the function fails due to a transient error, you can return PDH_RETRY and PDH will call your callback immediately.

Otherwise, return an appropriate error code. The error code is passed back to the caller of <a href="https://msdn.microsoft.com/4e9e4b20-a573-4f6d-97e8-63bcc675032b">PdhBrowseCounters</a>.




## -remarks



The following members of the 
<a href="https://msdn.microsoft.com/8e045e0b-c157-4527-902c-6096c7922642">PDH_BROWSE_DLG_CONFIG</a> structure are used to communicate with the callback function:






## -see-also




<a href="https://msdn.microsoft.com/8e045e0b-c157-4527-902c-6096c7922642">PDH_BROWSE_DLG_CONFIG</a>



<a href="https://msdn.microsoft.com/4e9e4b20-a573-4f6d-97e8-63bcc675032b">PdhBrowseCounters</a>
 

 

