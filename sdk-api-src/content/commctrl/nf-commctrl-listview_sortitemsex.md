---
UID: NF:commctrl.ListView_SortItemsEx
title: ListView_SortItemsEx macro
author: windows-sdk-content
description: Uses an application-defined comparison function to sort the items of a list-view control. The index of each item changes to reflect the new sequence. You can use this macro or send the LVM_SORTITEMSEX message explicitly.
old-location: controls\ListView_SortItemsEx.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_sortitemsex.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ListView_SortItemsEx, ListView_SortItemsEx macro [Windows Controls], _win32_ListView_SortItemsEx, _win32_ListView_SortItemsEx_cpp, commctrl/ListView_SortItemsEx, controls.ListView_SortItemsEx, controls._win32_ListView_SortItemsEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_SortItemsEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SortItemsEx macro


## -description


Uses an application-defined comparison function to sort the items of a list-view control. The index of each item changes to reflect the new sequence. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761228(v=VS.85).aspx">LVM_SORTITEMSEX</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param _pfnCompare

Type: <b>PFNLVCOMPARE</b>

A pointer to an application-defined comparison function. It is called during the sort operation each time the relative order of two list items needs to be compared. 


### -param _lPrm

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The application-defined value that is passed to the comparison function. 


## -remarks



The comparison function has the following form. 

<pre class="syntax" xml:space="preserve"><code>int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);</code></pre>
where 
				<i>lParam1</i> is the index of the first item and 
				<i>lParam2</i> the index of the second. The 
				<b>ListView_SortItemsEx</b>'s 
				<i>lParamSort</i> parameter is passed to the callback function as its third parameter.

The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent. 

You can send an <a href="https://msdn.microsoft.com/en-us/library/Bb761055(v=VS.85).aspx">LVM_GETITEMTEXT</a> message to retrieve further information on an item, if needed.

This macro is similar to <a href="https://msdn.microsoft.com/en-us/library/Bb775131(v=VS.85).aspx">ListView_SortItems</a>, except for the type of information passed to the comparison function. With <b>ListView_SortItemsEx</b>, the item's index is passed instead of its 
				<i>lparam</i> value. 

<div class="alert"><b>Note</b>   During the sorting process, the list-view contents are unstable. If the callback function sends any messages to the list-view control aside from <a href="https://msdn.microsoft.com/en-us/library/Bb774953(v=VS.85).aspx">LVM_GETITEM</a> (<a href="https://msdn.microsoft.com/en-us/library/Bb761308(v=VS.85).aspx">ListView_GetItem</a>), the results are unpredictable.</div>
<div> </div>


