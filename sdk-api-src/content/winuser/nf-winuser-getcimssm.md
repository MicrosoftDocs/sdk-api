---
UID: NF:winuser.GetCIMSSM
title: GetCIMSSM function (winuser.h)
author: windows-sdk-content
description: Retrieves the source of the input message (GetCurrentInputMessageSourceInSendMessage).
old-location: input_sourceid\getcimssm.htm
tech.root: Input_SourceId
ms.assetid: DF5C9B54-0B32-44D8-BFF6-80A190DC5294
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCIMSSM, GetCIMSSM function, input_sourceid.getcimssm, winuser/GetCIMSSM
ms.topic: function
f1_keywords: 
 - "winuser/GetCIMSSM"
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
ms.custom: 19H1
---

# GetCIMSSM function


## -description


<p class="CCE_Message">[<b>GetCIMSSM</b> may be altered or unavailable in the future. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getcurrentinputmessagesource">GetCurrentInputMessageSource</a>.]

Retrieves the source of the input message (GetCurrentInputMessageSourceInSendMessage).


## -parameters




### -param inputMessageSource [out]

The <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-taginput_message_source">INPUT_MESSAGE_SOURCE</a> structure that holds the device type and the ID of the input message source.


## -returns



If this function succeeds, it returns TRUE. Otherwise, it returns ERROR_INVALID_PARAMETER.

This function fails when:<ul>
<li>The input parameter is invalid.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getcurrentinputmessagesource">GetCurrentInputMessageSource</a> returns a value other than <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ne-winuser-taginput_message_device_type">IMDT_UNAVAILABLE</a> for the device type.</li>
</ul>





## -remarks



<b>GetCIMSSM</b> should be used only when <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getcurrentinputmessagesource">GetCurrentInputMessageSource</a> returns a device type of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ne-winuser-taginput_message_device_type">IMDT_UNAVAILABLE</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_sourceid/input-source-identification-reference">Input Source Identification Reference</a>
 

 

