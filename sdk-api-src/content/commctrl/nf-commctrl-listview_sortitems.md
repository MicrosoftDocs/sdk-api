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

# ListView_SortItems macro


## -description


Uses an application-defined comparison function to sort the items of a list-view control. The index of each item changes to reflect the new sequence. You can use this macro or send the <a href="https://msdn.microsoft.com/ed3d5cec-69af-49a1-9cb7-eb5da1163071">LVM_SORTITEMS</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param _pfnCompare

Type: <b>PFNLVCOMPARE</b>

A pointer to the application-defined comparison function. The comparison function is called during the sort operation each time the relative order of two list items needs to be compared. 


### -param _lPrm

TBD






#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


#### - lParamSort

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The application-defined value that is passed to the comparison function. 


## -remarks



The comparison function has the following form.

<pre class="syntax" xml:space="preserve"><code>int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);</code></pre>
The 
				<i>lParam1</i> parameter is the value associated with the first item being compared; and the 
				<i>lParam2</i> parameter is the value associated with the second item. These are the values that were specified in the 
				<b>lParam</b> member of the items' <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure when they were inserted into the list. The <i>lParamSort</i> parameter is the same value passed to the <a href="https://msdn.microsoft.com/ed3d5cec-69af-49a1-9cb7-eb5da1163071">LVM_SORTITEMS</a> message. 

The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent. 

<div class="alert"><b>Note</b>   During the sorting process, the list-view contents are unstable. If the callback function sends any messages to the list-view control, the results are unpredictable.</div>
<div> </div>


