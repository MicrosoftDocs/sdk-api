---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# AUTO_SCROLL_DATA structure


## -description


<p class="CCE_Message">[<b>AUTO_SCROLL_DATA</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Specifies scrolling parameters and keeps track of the last scroll operation.


## -struct-fields




### -field iNextSample

Type: <b>int</b>

A value that indicates the number of times the <a href="https://msdn.microsoft.com/3c5af682-8497-477e-8222-3eb37d1e295f">DAD_AutoScroll</a> function has stored data in the structure. The parameter is reset to <code>0</code> after it equals 2.


### -field dwLastScroll

Type: <b>DWORD</b>

A <b>DWORD</b> that indicates the time of the last scroll. The scroll time is also stored in the <b>dwTimes</b> parameter indexed by the current value of <b>iNextSample</b>.


### -field bFull

Type: <b>BOOL</b>

A value that is used to determine whether the <a href="https://msdn.microsoft.com/3c5af682-8497-477e-8222-3eb37d1e295f">DAD_AutoScroll</a> function should succeed. This parameter is set to <b>TRUE</b> when the <b>iNextSample</b> parameter is equal to NUM_POINTS.



#### (FALSE)

Default. Indicates that the window should not scroll.



#### (TRUE)

Indicates that the window should scroll.


### -field pts

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>[NUM_POINTS]</b>

A pointer to the current scroll coordinates. The index of this array is <b>iNextSample</b>.



### -field dwTimes

Type: <b>DWORD[NUM_POINTS]</b>

A <b>DWORD</b> that indicates the current scroll time. The index of this array is <b>iNextSample</b>.


## -remarks



NUM_POINTS is currently set to <code>3</code>.




## -see-also




<a href="https://msdn.microsoft.com/3c5af682-8497-477e-8222-3eb37d1e295f">DAD_AutoScroll</a>
 

 

