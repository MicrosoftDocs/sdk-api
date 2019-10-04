---
UID: NF:msinkaut.IInkCollector.GetEventInterest
title: IInkCollector::GetEventInterest (msinkaut.h)
author: windows-sdk-content
description: Retrieves the interest an object has in a particular event for the InkCollector class, InkOverlay class, or InkPicture class.
old-location: tablet\inkcollector_geteventinterest.htm
tech.root: tablet
ms.assetid: 532a798e-b434-4730-8c20-7ec60255f170
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 532a798e-b434-4730-8c20-7ec60255f170, GetEventInterest, GetEventInterest method [Tablet PC], GetEventInterest method [Tablet PC],IInkCollector interface, IInkCollector interface [Tablet PC],GetEventInterest method, IInkCollector.GetEventInterest, IInkCollector::GetEventInterest, msinkaut/IInkCollector::GetEventInterest, tablet.inkcollector_geteventinterest
ms.topic: method
f1_keywords: 
 - "msinkaut/IInkCollector.GetEventInterest"
dev_langs:
 - c++
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkCollector.GetEventInterest
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkCollector::GetEventInterest


## -description



Retrieves the interest an object has in a particular event for the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> class, <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> class, or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> class.




## -parameters




### -param EventId [in]

The event this method checks the interest of.


### -param Listen [out, retval]

<b>VARIANT_BOOL</b> if interest in the specified event has been set; otherwise, <b>VARIANT_FALSE</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid event interest.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred during processing.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846796(v=VS.85).aspx">IInkCollector</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectoreventinterest">InkCollectorEventInterest Enumeration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest">SetEventInterest Method</a>
 

 

