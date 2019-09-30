---
UID: NS:tapi.linemediacontroldigit_tag
title: LINEMEDIACONTROLDIGIT (tapi.h)
author: windows-sdk-content
description: The LINEMEDIACONTROLDIGIT structure describes a media action to be executed when detecting a digit. It is used as an entry in an array. The lineSetMediaControl and TSPI_lineSetMediaControl functions use this structure.
old-location: tapi2\linemediacontroldigit_str.htm
tech.root: Tapi
ms.assetid: d31cd365-d6a6-4595-8202-87113035d807
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPLINEMEDIACONTROLDIGIT, LINEMEDIACONTROLDIGIT, LINEMEDIACONTROLDIGIT structure [TAPI 2.2], LPLINEMEDIACONTROLDIGIT, LPLINEMEDIACONTROLDIGIT structure pointer [TAPI 2.2], _tapi2_linemediacontroldigit_str, tapi/LINEMEDIACONTROLDIGIT, tapi/LPLINEMEDIACONTROLDIGIT, tapi2.linemediacontroldigit_str"
ms.topic: struct
f1_keywords: 
 - "tapi/LINEMEDIACONTROLDIGIT"
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEMEDIACONTROLDIGIT
targetos: Windows
req.typenames: LINEMEDIACONTROLDIGIT, *LPLINEMEDIACONTROLDIGIT
req.redist: 
ms.custom: 19H1
---

# LINEMEDIACONTROLDIGIT structure


## -description


The 
<b>LINEMEDIACONTROLDIGIT</b> structure describes a media action to be executed when detecting a digit. It is used as an entry in an array. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linesetmediacontrol">lineSetMediaControl</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediacontrol">TSPI_lineSetMediaControl</a> functions use this structure.


## -struct-fields




### -field dwDigit

Low-order byte is the digit in whose detection is to trigger a media action. Valid digits depend on the media type.


### -field dwDigitModes

Digit mode(s) to monitor. This member uses one or more of the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/linedigitmode--constants">LINEDIGITMODE_ Constants</a>.


### -field dwMediaControl

Media control action. This member uses one of the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/linemediacontrol--constants">LINEMEDIACONTROL_ Constants</a>.


## -remarks



This structure may not be extended.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linemediacontrolmedia">LINEMEDIACONTROLMEDIA</a> structure defines a triple &lt;digit, digit mode(s), media-control action&gt;. An array of these triples is passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linesetmediacontrol">lineSetMediaControl</a> function to set the media control actions triggered by digits detected on a given call. When a listed digit is detected, then the corresponding action on the media stream is invoked.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linemediacontrolmedia">LINEMEDIACONTROLMEDIA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediacontrol">TSPI_lineSetMediaControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linesetmediacontrol">lineSetMediaControl</a>
 

 

