---
UID: NF:winuser.GetCIMSSM
title: GetCIMSSM function
author: windows-sdk-content
description: Retrieves the source of the input message (GetCurrentInputMessageSourceInSendMessage).
old-location: input_sourceid\getcimssm.htm
tech.root: Input_SourceId
ms.assetid: DF5C9B54-0B32-44D8-BFF6-80A190DC5294
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCIMSSM, GetCIMSSM function, input_sourceid.getcimssm, winuser/GetCIMSSM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetCIMSSM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCIMSSM function


## -description


<p class="CCE_Message">[<b>GetCIMSSM</b> may be altered or unavailable in the future. Instead, use <a href="https://msdn.microsoft.com/35e4ebf5-df9d-4168-9996-355204c2ab93">GetCurrentInputMessageSource</a>.]

Retrieves the source of the input message (GetCurrentInputMessageSourceInSendMessage).


## -parameters




### -param inputMessageSource [out]

The <a href="https://msdn.microsoft.com/75437c0a-925a-44d9-9254-43095b281c21">INPUT_MESSAGE_SOURCE</a> structure that holds the device type and the ID of the input message source.


## -returns



If this function succeeds, it returns TRUE. Otherwise, it returns ERROR_INVALID_PARAMETER.

This function fails when:<ul>
<li>The input parameter is invalid.</li>
<li>
<a href="https://msdn.microsoft.com/35e4ebf5-df9d-4168-9996-355204c2ab93">GetCurrentInputMessageSource</a> returns a value other than <a href="https://msdn.microsoft.com/aaaa8d9b-1056-4fa3-afcf-43d2c4b41c0e">IMDT_UNAVAILABLE</a> for the device type.</li>
</ul>





## -remarks



<b>GetCIMSSM</b> should be used only when <a href="https://msdn.microsoft.com/35e4ebf5-df9d-4168-9996-355204c2ab93">GetCurrentInputMessageSource</a> returns a device type of <a href="https://msdn.microsoft.com/aaaa8d9b-1056-4fa3-afcf-43d2c4b41c0e">IMDT_UNAVAILABLE</a>.




## -see-also




<a href="https://msdn.microsoft.com/1B1292B2-1BB6-4F75-8D82-CC0596B9D061">Input Source Identification Reference</a>
 

 

