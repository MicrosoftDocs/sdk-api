---
UID: NF:strmif.IAMPushSource.SetPushSourceFlags
title: IAMPushSource::SetPushSourceFlags
author: windows-driver-content
description: The SetPushSourceFlags method sets flags that specify the behavior of the filter. Currently, applications should not call this method, because request flags are not supported and an application should not override the flags set by the filter.
old-location: dshow\iampushsource_setpushsourceflags.htm
old-project: DirectShow
ms.assetid: c07bbf7e-8d81-4eba-a5a1-fde02e8e8c35
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMPushSource interface [DirectShow],SetPushSourceFlags method, IAMPushSource.SetPushSourceFlags, IAMPushSource::SetPushSourceFlags, IAMPushSourceSetPushSourceFlags, SetPushSourceFlags, SetPushSourceFlags method [DirectShow], SetPushSourceFlags method [DirectShow],IAMPushSource interface, dshow.iampushsource_setpushsourceflags, strmif/IAMPushSource::SetPushSourceFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMPushSource.SetPushSourceFlags
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMPushSource::SetPushSourceFlags


## -description



The <code>SetPushSourceFlags</code> method sets flags that specify the behavior of the filter. Currently, applications should not call this method, because request flags are not supported and an application should not override the flags set by the filter.




## -parameters




### -param Flags [in]

Combination of flags from the <a href="https://msdn.microsoft.com/878dc41b-8df3-4294-9e1f-7a3da1834ad1">AM_PUSHSOURCE_FLAGS</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5ab294a8-f250-405c-a589-68998bc04cdf">IAMPushSource Interface</a>
 

 

