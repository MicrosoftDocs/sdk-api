---
UID: NF:winddi.EngQueryLocalTime
title: EngQueryLocalTime function
author: windows-sdk-content
description: The EngQueryLocalTime function queries the local time.
old-location: display\engquerylocaltime.htm
old-project: display
ms.assetid: 826993fc-7cf2-4747-a0d9-086e5d7310b6
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: EngQueryLocalTime, EngQueryLocalTime function [Display Devices], display.engquerylocaltime, gdifncs_268682b0-aef3-4241-b49c-1cea87ec4f29.xml, winddi/EngQueryLocalTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngQueryLocalTime
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngQueryLocalTime function


## -description


The <b>EngQueryLocalTime</b> function queries the local time.


## -parameters




### -param Arg1 [out]

Pointer to an <a href="https://msdn.microsoft.com/482e1d15-d499-4ed2-87e7-760f03a454b5">ENG_TIME_FIELDS</a> structure that receives the local time.


## -returns



None




## -remarks



<b>EngQueryLocalTime</b> returns the time at the current locale in the ENG_TIME_FIELDS structure.




## -see-also




<a href="https://msdn.microsoft.com/482e1d15-d499-4ed2-87e7-760f03a454b5">ENG_TIME_FIELDS</a>
 

 

