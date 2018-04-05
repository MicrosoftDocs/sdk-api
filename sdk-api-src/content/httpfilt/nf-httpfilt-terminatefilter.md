---
UID: NF:httpfilt.TerminateFilter
title: TerminateFilter function
author: windows-driver-content
description: The TerminateFilter function indicates to the filter that it will be removed from memory. When this function is called, you should make sure that the filter closes any attachments it has made to system resources.
old-location: tmg\terminatefilter.htm
old-project: TMG
ms.assetid: e1b14756-6df1-4944-a34b-1d739b0f0ca4
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: TerminateFilter, TerminateFilter callback function [Forefront TMG], httpfilt/TerminateFilter, tmg.terminatefilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: httpfilt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported,Forefront Threat Management Gateway (TMG) 2010
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 (64-bit only) [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: HTTP_VERSION, *PHTTP_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Httpfilt.h
api_name:
-	TerminateFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# TerminateFilter function


## -description


The  <b>TerminateFilter</b> function indicates to the filter that it will be removed from memory. When this function is called, you should make sure that the filter closes any attachments it has made to system resources.

The 
<b>TerminateFilter</b> function is declared as:


## -parameters




### -param dwFlags [in]

No values for the <i>dwFlags</i> parameter have been identified at this time.


## -see-also




<a href="https://msdn.microsoft.com/371c9784-7d7a-4020-8e49-a8b6a72f2b5c">Entry-Point Functions</a>
 

 

