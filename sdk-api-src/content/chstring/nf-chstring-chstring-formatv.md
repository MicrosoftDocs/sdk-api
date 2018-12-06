---
UID: NF:chstring.CHString.FormatV
title: CHString::FormatV
author: windows-sdk-content
description: The FormatV method writes a formatted string and a variable list of arguments to a CHString string.
old-location: wmi\chstring_formatv.htm
tech.root: WmiSdk
ms.assetid: 55488cf0-0098-4d5b-b451-a5d56f30ed65
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "?FormatV@CHString@@QAEXPBGPAD@Z, ?FormatV@CHString@@QEAAXPEBGPEAD@Z, CHString interface [Windows Management Instrumentation],FormatV method, CHString.FormatV, CHString::FormatV, FormatV, FormatV method [Windows Management Instrumentation], FormatV method [Windows Management Instrumentation],CHString interface, _hmm_chstring_formatv, chstring/CHString::FormatV, wmi.chstring_formatv"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: chstring.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString.FormatV
 - ?FormatV@CHString@@QAEXPBGPAD@Z
 - ?FormatV@CHString@@QEAAXPEBGPEAD@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHString::FormatV


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>FormatV</b> method writes a formatted string and a variable list of arguments to a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string.


## -parameters




### -param lpszFormat

Format control string.


### -param argList

List of arguments that are passed.


## -returns



This method does not return a value.




## -remarks



The <b>FormatV</b> method formats and stores a series of characters and values in the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string. The string and arguments are converted and output according to the corresponding format specification in <i>lpszFormat</i>.

If the string object is offered as a parameter to <b>FormatV</b>, the call fails.

<div class="alert"><b>Note</b>  To reduce exposure to security attacks, always use a format string for <b>FormatV</b>. Never use a user-supplied string for the format string. If your format string is stored for a purpose such as localization, ensure that the string is protected from unauthorized write access. If your function writes to a string rather than standard output, you may need to avoid using a trailing "%s" in the format string. For more information, see <a href="Http://go.microsoft.com/fwlink/p/?linkid=84443">www.securityfocus.com/archive/1/81565</a> and <a href="Http://go.microsoft.com/fwlink/p/?linkid=84442">www.securityfocus.com/archive/1/66842</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/95d24b0e-3580-4a5d-8dad-50d44ef1ca39">CHString::Format</a>
 

 

